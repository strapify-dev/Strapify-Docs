# strapi-single-type-class-add

The `strapi-single-type-class-add` attribute works much the same as [strapi-class-add](../css-modifiers/strapi-class-add.md) attribute, but can be used on a single type element instead of a collection element.

This attribute will cause the value of a Strapi single type field to be added to an element’s class list.

Below is the HTML to render a the Strapi single type field company_name of the single type collection info. The `strapi-single-type-class-add` attribute causes the value of the field company_name_color_class from the info collection to be added to the `h1` element’s class list.

**Allows Multiple Arguments:** ✅ **YES**

### Example

```html
<h1
	strapi-single-type-field="info.company_name"
	strapi-class-add="info.company_name_color_class"
>
	company name
</h1>
```

