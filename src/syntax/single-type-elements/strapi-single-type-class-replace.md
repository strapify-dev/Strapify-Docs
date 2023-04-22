# strapi-single-type-class-replace

The `strapi-single-type-class-replace` attribute works much the same as [strapi-class-replace](../css-modifiers/strapi-class-replace.md) attribute, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the value of a Strapi single type field to be added to an element’s class list, replacing an the specified existing class.

```html
<h1
	strapi-single-type-field="info.company_name"
	strapi-class-replace="info.company_name_color_class, black"
>
	company name
</h1>
```