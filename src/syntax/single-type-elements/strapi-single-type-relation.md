# strapi-single-type-relation

The `strapi-single-type-relation` attribute works much the same as the [strapi-relation](../relations-and-repeatables/strapi-relation.md) attribute, but is used on single types instead of collection types. It also does not need to exist as a child of a template element, unlike the strapi-relation attribute.

Below is the HTML to render the single type field employees which belongs to the Company single type. The employees field is a relation with the collection Person (people).

```html
<div strapi-single-type-relation="Company.employees, people">
	<div strapi-template="">
		<p strapi-field="name">employee name goes here</p>
		<p strapi-field="age">employee age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

See above