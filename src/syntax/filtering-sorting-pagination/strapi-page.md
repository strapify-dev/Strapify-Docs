# strapi-page

The `strapi-page` attribute is used to specify a which page Strapify will fetch from Strapi. The default value is 1. When an out of bounds page index is given, Strapify will automatically convert it to the nearest valid index.

Strapify will reflect changes to this attribute automatically if it is changed with a script.

Below is the HTML to render the second page of the collection Person (plural people), with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-page="2">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

### Examples

```html
<div strapi-collection="people" strapi-page="1">
```

The collection "people" will be rendered with the first page of the collection.

```html
<div strapi-collection="people" strapi-page="2">
```

The collection "people" will be rendered with the second page of the collection.