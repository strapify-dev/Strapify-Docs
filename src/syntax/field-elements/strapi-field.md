# strapi-field

The `strapi-field` attribute specifies that the element is a [field element](./index.md). Elements with strapi-field will have their content replaced with content from Strapi.  How and which content of the field elements are modified is contextual and depends on the element tag and the strapi field type being used.

Below is the HTML to render a collection Person (plural people), with several different element types to render Strapi fields.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name</p>
		<p strapi-field="age">age</p>
		<p>is employed: <span strapi-field="is_employed">is_employed</span></p>
		<div strapi-field="bio">
			<p>rich text placeholder ( I get deleted ) )</p>
		</div>
		<img strapi-field="portrait" />
	</div>
</div>
```

| Strapi Field Type | HTML Elements | Comments                                                                                                                                                                               |
| ----------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Text              | `p` `h` `span` `div`  | The div is typically invalid but can be used as a special case to embed a video. For it to work, your text field must contain a link and the div must contain an iframe child element. |
| Email             | `p` `h` `span`      | Field data will be inserted as text content.                                                                                                                                           |
| Rich Text         | `div`           | HTML elements will be created in the div to render the rich text.                                                                                                                      |
| Number            | `p` `h` `span`      | Field data will be inserted as text content.                                                                                                                                           |
| Enumeration       | `p` `h` `span`      | Field data will be inserted as text content.                                                                                                                                           |
| Date              | `p` `h` `span`      | Field data will be inserted as text content.                                                                                                                                           |
| Media (Image)     | `img`           | The image source will be set to point to the Strapi url for the image.                                                                                                                 |
| Media (Video)     | `div`           | A video element will be inserted into the div.                                                                                                                                         |
| Boolean           | `p` `h` `span`      | Field data will be inserted as text content.                                                                                                                                           |

For relations see `strapi-relation`, for repeatable components or multiple media type fields see `strapi-repeatable`.  

Field elements must be a child of a [template element](syntax/template-elements/index.md) or be a template element. 

**Allowed Elements:**

`div` `p` `h` `span` `img`

**Related Attributes:**

[strapi-template](../template-elements/strapi-template.md)

**Allows Multiple Arguments:** 🚫 **NO**

### Examples

```html
<p>Name: <span strapi-field="name">name</span></p>
```
Renders the value in the Strapi field name.

```html
<img strapi-field="portrait_image">
```
Renders the image held in the Strapi field portrait_image.

```html
<p>First Name: <span strapi-field="name.first">first name</span></p>
```
Renders the field first in the component field name.