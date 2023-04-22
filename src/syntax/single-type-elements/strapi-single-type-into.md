# strapi-single-type-into

The `strapi-single-type-into` attribute is used to pass data from a Strapi single type collection field directly into an HTML attribute.

Below is the HTML to set the alt text of the `img` element to the value held in the Strapi single type field `alt_text`.

```html
<img
	strapi-single-type-field="info.company_image"
	strapi-into="info.company_image_alt_text -> alt"
/>
```

**Allowed Elements:**

Any.

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

```html
<img
    strapi-single-type-field="info.company_image"
    strapi-into="info.company_image_alt_text -> alt"
/>
```

Sets the alt attribute of the img element to the value in the strapi single type field alt_text of the collection info.

```html
<img
    strapi-single-type-field="home_page"
    strapi-into="home_page.element_id -> id | home_page.alt_text -> alt"
/>
```

Sets the id of the img element to the value in the Strapi single type field element_id and sets the alt attribute of the img element to the value in the Strapi single type field alt_text of the collection home_page.