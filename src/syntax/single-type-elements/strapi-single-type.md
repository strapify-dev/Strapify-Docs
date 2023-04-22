# strapi-single-type

The `strapi-single-type` attribute works much the same as `strapi-field`, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the value of a Strapi single type field to be rendered in the element.

| Strapi Field Type | HTML Elements | Comments                                                                                                                                                                               |
| ----------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Text              | p h span div  | The div is typically invalid but can be used as a special case to embed a video. For it to work, your text field must contain a link and the div must contain an iframe child element. |
| Email             | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Rich Text         | div           | HTML elements will be created in the div to render the rich text.                                                                                                                      |
| Number            | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Enumeration       | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Date              | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Media (Image)     | img           | The image source will be set to point to the Strapi url for the image.                                                                                                                 |
| Media (Video)     | div           | A video element will be inserted into the div.                                                                                                                                         |
| Boolean           | p h span      | Field data will be inserted as text content.                                                                                                                                           |

Below is the HTML to render a few fields from the single type collection info.

```html
<div>
	<h1 strapi-single-type="info.company_name">Company Name</h1>
	<img strapi-single-type="info.company_image" />
	<div strapi-single-type="info.bio">
		<p>placeholder for bio<p>
	</div>
</div
```

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

```html
<p strapi-single-type="info.name"></p>
```
Render the value in the Strapi single type field name for the single type collection info.

```html
<p strapi-single-type="home_page.title"></p>
```
Render the value in the Strapi single type field title for the single type collection home_page.

```html
<p strapi-single-type="home_page.article.title"></p>
```
Render the value in title, which is an element of a component called article which belongs to the home_page single type collection.