# Strapify Conditional Expression Arguments

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