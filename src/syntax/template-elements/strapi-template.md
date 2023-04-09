# strapi-template

The `strapi-template` attribute specifies that the element is a template element. All template elements will be removed from the DOM when Strapify runs and replaced with template elements injected with Strapi data. Template elements must exist as children of collection elements, relation elements or repeatable elements.  If multiple template elements exist as children to a collection element, relation element or repeatable element, the first occurring template element will be used. 

If a collection element, relation element or repeatable element contains a standard template in addition to conditional template elements, any Strapi entries that don’t meet the conditions for any of the conditional templates, will use the standard template as a fallback.

Below is the HTML to specify a template element for the collection people, with two `p` elements to render the name and age fields.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

Any element.

**Related Attributes:**

[strapi-template-conditional](./strapi-template-conditional.md)

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

```html
<div strapi-template="">
	<p strapi-field="name">name goes here</p>
	<p strapi-field="age">age goes here</p>
</div>
```

Mark the div element as a template element for the Strapi collection named my_strapi_collection_name_plural.