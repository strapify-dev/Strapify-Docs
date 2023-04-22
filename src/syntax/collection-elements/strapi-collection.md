# strapi-collection

The `strapi-collection` attribute specifies that the element is a [collection element](index.md). The value of this attribute is the plural API id of a Strapi collection. 

Strapify will search the element for a template element or a set of template elements if there are conditional template elements, they will be replicated for each entry in the collection.

If multiple template elements exist as children to the collection element, the first occurring template element will be used. If there are two conditional template elements with equivalent conditions, existing as children to the collection element, the first occurrence will be used. All template elements will be removed from the DOM when Strapify runs (you can have many copies of your template to help visualize how your site will look during development, Strapify will remove them for you). Any elements existing as children to the collection element that is not a template element, will be left untouched (you can put text, links, buttons or other things within collection elements).

If the collection element contains a standard template in addition to conditional template elements, any Strapi entries that don’t meet the conditions for any of the conditional templates will use the standard template.

---

Below is the HTML to render a collection called Person (people), with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```