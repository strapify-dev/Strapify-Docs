# strapi-background-image

The `strapi-background-image` attribute is used to set a background image on another element. The value of the attribute is the name of the Strapi field that contains the image. The image must be a single image, not multiple images.

The CSS background-size is set to cover by default. To override this, you'll need to use `!important` in your CSS.

Below is an HTML example of the `strapi-background-image` attribute being used to set the background image of a div.

```html
<div strapi-collection="countries">
	<div strapi-template="" strapi-background-image="countryImage">
		<h1 strapi-field="countryName"></h1>
	</div>
</div>
```

**Allowed Elements:**

Any template element or child of a template element.

**Related Attributes:**

[strapi-field](strapi-field.md)

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

```html
<div strapi-template strapi-background-image="portraitPhoto">
	<h3 strapi-field="name"></h3>
</div>
```
Sets the background image of the div to the value in the strapi field "portraitPhoto".

```html
<div strapi-template>
	<div strapi-background-image="portraitPhoto"></div>
	<h3 strapi-field="name"></h3>
</div>

```

Sets the background image of the div to the value in the strapi field "portraitPhoto".
