# strapi-page-size

The `strapi-page-size` attribute is used to specify the size of pages when data is fetched from Strapi. When unspecified Strapi’s default size will be used (25).

Strapify will reflect changes to this attribute automatically if it is changed with a script.

Below is the HTML to render a collection called Person (plural people), with a page size of 5, with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-page="1" strapi-page-size="5">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

### Examples

```html
<div strapi-collection="people" strapi-page-size="5">
```

The collection "people" will be rendered with a page size of 5.

```html
<div strapi-collection="people" strapi-page-size="10">
```

The collection "people" will be rendered with a page size of 10.