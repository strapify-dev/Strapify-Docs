# strapi-hide-on-fail

The `strapi-hide-on-fail` attribute will cause a collection element, relation element or repeatable element to be hidden in the case that an error occurred when fetching data. This attribute is useful in scenarios for which failure is expected, such as when the collection is only available to authenticated users but the current user has not yet authenticated. It may also be used to hide data if there is an unexpected error, but state elements should be preferred in such cases.

Strapify currently accomplishes this by adding a class with CSS attribute `display: none;` on the element. It will not work if you have specified the CSS display attribute inline or with !important.

Below is the HTML to hide a collection in the case that there is an error retrieving the collection data.

```html
<div strapi-collection="people" strapi-hide-on-fail="">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

```html
<div strapi-collection="people" strapi-hide-on-fail>
    <div strapi-template>
        The template to be hidden if there is an error
        <p strapi-field="name">name goes here</p>
        <p strapi-field="age">age goes here</p>
    </div>
```
Strapify will attempt to render the collection People. If an error occurs, the element will become hidden.