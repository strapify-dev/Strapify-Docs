# strapi-relation

The `strapi-relation` attribute specifies that the element is a relation element. Relation elements function identically to collection elements, except they are automatically filtered to only retrieve entries in the collection in the relation. Like collection elements, relation elements must contain templates. The field elements in those templates will reference fields existing on entries of the related collection. The argument must provide both the name of the relation field and the name of the collection being related, separated by a comma.

Below is the HTML to render the collection people, which has a relation with itself to define each person’s children. Each child of a person will have their name and age rendered.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>

		<div strapi-relation="children, people">
			<div strapi-template="">
				<p strapi-field="name">child name goes here</p>
				<p strapi-field="age">child age goes here</p>
			</div>
		</div>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

### Examples

```html
<div strapi-relation="children, people">
```

Marks the div element as a relation element with the relation defined in the field children for the collection called people.

```html
<div strapi-relation="pets, animals">
```

Marks the div element as a relation element with the relation defined in the field pets for the collection called animals.