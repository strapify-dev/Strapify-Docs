# Components in Arguments

To reference a Strapi field contained in a component, you write the field name of the component and then the name of the field in the component, separated by a **.** (period). For example,

`strapi-field="name.first"`

would refer to the field with field name _first_ within the component with field name _name._

This also works with nested components like so

`strapi-field="employee.name.first"`

which refers to a field called _first_ which exists within a component _name_ which exists within a component _employee_.