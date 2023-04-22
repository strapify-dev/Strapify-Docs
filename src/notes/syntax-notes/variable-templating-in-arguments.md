# Variable Templating in Arguments

Some attributes (see below) accept a template as an argument; a string which may contain references to Strapi fields. Strapi fields are referenced by giving the field name wrapped in double curly braces `{{}}`.

For example,

`background: {{background_color}};` would be transformed into `background: red;`.

An attribute using the above template would look like this,

`strapi-css-rule="background: {{background_color}};"`.

This attribute would create an inline CSS rule for the element, with a substitution of the value held in the Strapi field background_color in place of `{{background_color}}`.

Attributes that accept variable template arguments:

`strapi-into`, `strapi-css-rule`, `strapi-single-type-into`, `strapi-single-type-css-rule`