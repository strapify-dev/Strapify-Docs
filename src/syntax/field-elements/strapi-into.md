# strapi-into

The `strapi-into` attribute is used to pass data from a Strapi field directly into an HTML attribute. Elements with this attribute must belong to a template element.

Below is the HTML to render a collection Person (plural people), with a `strapi-into` attribute to set the alt text of the `img` to the value held in the Strapi field `alt_text`.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<img strapi-field="portrait" strapi-into="alt_text -> alt" />
	</div>
</div>
```

**Allowed Elements:**

Any.

**Related Attributes:**

[strapi-field](strapi-field.md)

**Allows Multiple Arguments:** ✅ **YES**

### Examples

```html
<img strapi-into="alt_text -> alt">
```

Sets the alt attribute of the img element to the value in the strapi field alt_text.

```html
<img strapi-into="image.alt_text -> alt">
```

Sets the alt attribute of the img element to the value in the field alt_text belonging to the component in the field image.

```html
<img strapi-into="element_id -> id | alt_text -> alt">
```

Sets the id of the img element to the value in the Strapi field element_id and sets the alt attribute of the img element to the value in the strapi field alt_text.