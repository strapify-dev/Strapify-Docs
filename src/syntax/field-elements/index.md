# Field Elements

_Field elements_ are HTML elements that will have their content modified with data from Strapi when Strapify executes. Each of these elements correspond to a particular field in a Strapi collection. These elements are defined with the `strapi-field` attribute. How and which content of the _field elements_ are modified is contextual and depends on the element tag and the strapi field type being used. Read through the attribute syntax for more details.

**Allowed Attributes:**

`strapi-field` `strapi-into` `strapi-class-add` `strapi-class-replace` `strapi-class-conditional`