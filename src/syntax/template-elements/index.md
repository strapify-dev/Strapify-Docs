# Template Elements

_Template elements_ are HTML elements that will be duplicated for each entry in a Strapi collection, relation or repeatable field (components, media, etc…). 

These elements contain [field elements](syntax/field-elements/index.md), and are descendants of [collection elements](syntax/collection-elements/index.md), [relation elements](syntax/relations-and-repeatables/strapi-relation.md) or [repeatable elements](syntax/relations-and-repeatables/strapi-repeatable.md). Template elements are defined with the `strapi-template` attribute. 

Multiple templates can be created and chosen dynamically based on the data in Strapi using `strapi-template-conditional`

Template elements also add a `strapi-template-id` attribute which can be used in cases where you need to fetch data directly from the Strapi API.

<!-- Once data has been inserted into a template, and that template has been added to the DOM, these elements will be referred to as _populated template elements_. You, as the developer, add _template elements_ to the website and Strapify will use those elements to create _populated template elements_ that the user will see at runtime. -->
#### Attributes

[strapi-template](./strapi-template.md), [strapi-template-conditional](./strapi-template-conditional.md)