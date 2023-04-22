# Arguments

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