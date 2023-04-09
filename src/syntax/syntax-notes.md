# Syntax Notes (Refactor to multiple sections)

### Arguments

An argument is the value you give to a strapi attribute when it is created. For example, in the following line,

`strapi-collection="cards"`

**_cards_** is said to be the argument.

In the next line,

`strapi-into="alt_text -> alt"`

**_alt_text → alt_** is said to be the argument*.*

There are a few important rules (conforming to the Strapi rest API) that should be remembered when referring to Strapi collection names and field names.:

- Collections are always described by their plural name: (**_cards_** is valid while **_card_** is not)
- If a collection name contains underscores, those underscores should be replaced with dashes when referring to the collection: (**_some-collection_** is valid while **_some_collection_** is not)
- Collection names are not case sensitive: (**_cards_** is equivalent to **_Cards)_**
- Field names are case sensitive: (**_name_** is NOT equivalent to **_Name_**)
- Field names should not have underscores replaced with dashes: (**_field_name_** is valid while **_field-name_** is not)

### Multiple Arguments

Some attributes such as `strapi-class-add`, can accept multiple arguments as a value. These arguments are given as | (vertical bar/pipe) separated values. When multiple arguments are given in an attribute value, Strapify will function as if two attributes of the same name but different values were given. For example,

    `strapi-class-add="layout-class | color-class"`

will cause both the class names given in the Strapi fields layout-class and color-class to be added to class list of the element containing the attribute. It is not valid to define two attributes of the same name on an element, so the | syntax must be used.

### Components in Arguments

To reference a Strapi field contained in a component, you write the field name of the component and then the name of the field in the component, separated by a **.** (period). For example,

`strapi-field="name.first"`

would refer to the field with field name _first_ within the component with field name _name._

This also works with nested components like so

`strapi-field="employee.name.first"`

which refers to a field called _first_ which exists within a component _name_ which exists within a component _employee_.

### Variable Templating in Arguments

Some attributes (see below) accept a template as an argument; a string which may contain references to Strapi fields. Strapi fields are referenced by giving the field name wrapped in double curly braces `{{}}`.

For example,

`background: {{background_color}};` would be transformed into `background: red;`.

An attribute using the above template would look like this,

`strapi-css-rule="background: {{background_color}};"`.

This attribute would create an inline CSS rule for the element, with a substitution of the value held in the Strapi field background_color in place of `{{background_color}}`.

Attributes that accept variable template arguments:

`strapi-into`, `strapi-css-rule`, `strapi-single-type-into`, `strapi-single-type-css-rule`

### Query String Variables in Arguments

Query string arguments are arguments that contain a placeholder for a value contained in the current page’s query string, notated by a **_qs._** prefix, example: **_qs.varName_**. When strapify finds an occurrence of a query string argument, it will be replaced entirely by the value of the query string parameter with the specified name. For example **_qs.varName_** would be replaced by **_varValue_** if the query string for the page was **_?varName=varValue_**. A few more examples are shown in the table below. Query string variables may be used in any Strapify attribute value.

| Website Query String      | Given Attribute Value      | Strapify Uses             |
| ------------------------- | -------------------------- | ------------------------- |
| ?message=hello            | qs.message                 | hello                     |
| ?nameComponentField=first | name.qs.nameComponentField | name.first                |
| ?title=movie review       | [title][$eq]=qs.title      | [title][$eq]=movie review |

There may be situations where you wish to render a single entry in a Strapi collection on a dedicated page. For example, if you had a collection Blogs, you may wish to have a separate page for each Blog belonging to Blogs. Strapify allows this situations through query string arguments, which you would write in the URL when you link to the page for the blog. Consider the following Strapi collection.

> collection name: Blog
>
> - field name: title
> - field name: rich_text

Now let’s say you want to have a page for a blog in the collection with title “fun day at the beach.” and another page for a blog with title “bad day at home.”. To do this create a page called www.yourwebsite.com/blog and on that page, create a collection element as you would normally. Now to link to that URL in a way that will allow you display only the “fun day at the beach blog”, you would use the URL www.yourwebsite.com/blog?title=fun day at the beach. On your blog page, the query string parameter will be available in your strapi arguments, which you can use to filter out a single blog to display. You would use the following attributes on the collection element your created:

`strapi-collection="blogs"` , `strapi-filter="[title][$eq]=qs.title"`

If you wanted to instead link to the blog with title “bad day at home”, you would use the URL www.yourwebsite.com/blog?title=bad day at home.

### Strapi Request Query Strings

Some attributes, such as `strapi-filter` and `strapi-sort` accept arguments arguments conforming to [Strapi query string API parameters](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/api-parameters.html). The syntax for these attributes is identical to the Strapi query string API, except the identifier for the query string parameter is omitted. For example, consider the query string parameter `sort=age` , which might appear in a Strapi request like _localhost:1337/api/people?sort=age_. To achieve this in strapify you would give the attribute `strapi-sort` the argument `age`. Similarly for filters, the query string parameter `filters[name][$eq]=Paul Dirac` would become `[name][$eq]=Paul Dirac` when used with a the `strapi-filter` attribute.

When making a Strapi request, it is possible to include multiple of the same query string parameter. For example, you might have a request like localhost:1337/api/people?sort=name&sort=age:desc which would would sort the collection people by name and then by age descending. This is accomplished in Strapify by providing multiple arguments to the `strapi-sort` attribute with the value `name | age:desc` . Filters work similarly, if you had the request url localhost:1337/api/people?filters[$and][0][name][$eq]=Paul Dirac&filters[$and][1][age][$eq]=82, you would give `strapi-filter` the value `[$and][0][name][$eq]=Paul Dirac | [$and][1][age][$eq]=82` .

There is one important difference between the Strapi query string API syntax and the Strapify syntax: equality operators must always be prefixed with `[$eq]` in Strapify arguments. For example, `[name][$eq]=Paul Dirac` is valid while `[name]=Paul Dirac` is not. This is due to the fact that while Strapi will allow the `[$eq]` part to be omitted when all other occurrences of the equality operator also omit it, Strapify uses the full `[$eq]=` syntax internally. If Strapify receives arguments using `=` instead of `[$eq]=` , invalid requests will be made and your Strapi data will not be fetched.

### Strapify Conditional Expression Arguments

There are Strapify attributes that require a conditional expression to be given as an argument, namely `strapi-template-conditional` and `strapi-class-conditional` . The conditional expressions are written using a syntax specific to Strapify. The syntax is similar to popular programming languages such as C, Java, Javascript and Python, though much more primitive. A Strapify conditional expression may contain operands, operators and groups. Operands are values which are to be compared to one another, using a comparison operator. Operators, such as `==` and `&&`, define how two operands or sub-expression groups are to be compared or logically composed. Groups are sub-expressions contained within round bracket parentheses, used to impose an order of logical operations. Strapify will take any Strapi data and query string variable data to make the specified comparisons to produce a boolean value representing whether or not the condition is met.

Below are the allowed operands types with a few examples:

- integer literals: `1` `32`
- float literals: `1.0` `54.43`
- string literals: `'hello world'` `'32'` `'true'` `' '`
- boolean literals: `true` `false`
- null literals: `null` `undefined`
- Strapi field variables: `age` `name.first` `is_employed`
- Strapify query string variables: `qs.title` `qs.queryStringVarName`

Below are the allowed operators with some examples:

- equality: `age == 24` `name == 'Paul Dirac'` `is_employed == false` `favorite_food == null` `name.first == name.last` `title == qs.title`
- not equal to: `age != 24` `name != 'Paul Dirac'` `is_employed != false` `score !=  3.5` `favorite_food != null`
- less than: `age < 33` `score < 8`
- less than or equal to: `age <= 33` `score <= 8`
- greater than: `age > 33` `score > 8`
- greater than or equal to: `age >= 33` `score >= 8`
- and: `name == 'Paul Dirac' && age == 82` `is_employed == true && favorite_food == 'Pizza'`
- or: `name == 'Paul Dirac' || age == 82` `is_employed == true || favorite_food == 'Pizza'`

Expressions must always be split into groups (with parentheses) when using more than one logical operator. The following are valid examples:

- `name == 'Paul Dirac' && age == 82`
- `(name == 'Paul Dirac' && age == 82) || is_employed == false`
- `(name == 'Paul Dirac' && age == 82) || (is_employed == false && score == 3.0)`

### Special Characters

- Note that some special characters including ampersands (&) should be encoded manually in your attribute values. For example if you’re trying to filter by a Category field equal to “Rice & Beans”, the value would be `strapi-filter=[Category][$eq]=Rice %26 Beans` rather than `strapi-filter=[Category][$eq]=Rice & Beans`
