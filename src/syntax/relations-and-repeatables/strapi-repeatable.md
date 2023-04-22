# strapi-repeatable

The `strapi-repeatable` attribute specifies that the element is a repeatable element. Repeatable elements function identically to collection elements, except their data is not pulled from a strapi collection but rather the data in a collection entries field. This attribute is used to render either multi-media fields (multiple images, multiple videos, …) or repeatable components. Like collection elements, repeatable elements must contain templates. The field elements in those templates must use the name of you repeatable field (see below).

Below is the HTML to render the collection people, with a multiple media field of images called my_images.

**Allows Multiple Arguments:** 🚫 **NO**

### Example

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>

		<div strapi-repeatable="my_images">
			<div strapi-template="">
				<img strapi-field="my_images" />
			</div>
		</div>
	</div>
</div>
```

The collection "people" will be rendered with a repeatable element for the field my_images.