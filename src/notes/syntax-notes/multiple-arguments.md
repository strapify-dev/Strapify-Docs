# Multiple Arguments

Some attributes such as `strapi-class-add`, can accept multiple arguments as a value. These arguments are given as | (vertical bar/pipe) separated values. When multiple arguments are given in an attribute value, Strapify will function as if two attributes of the same name but different values were given. For example,

    `strapi-class-add="layout-class | color-class"`

will cause both the class names given in the Strapi fields layout-class and color-class to be added to class list of the element containing the attribute. It is not valid to define two attributes of the same name on an element, so the | syntax must be used.
