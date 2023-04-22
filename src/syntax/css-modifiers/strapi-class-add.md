# strapi-class-add

The `strapi-class-add` attribute adds a class to an element with the name specified by the value in a Strapi field. These elements must exist as children of a template element. This allows the styling of elements to be changed through the Strapi CMS.

Below is the HTML to render a collection Person (plural people), with a `strapi-class-add` attribute to add a class to the `p` element, with the class decided by the value of the Strapi field color_class.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name" strapi-class-add="color_class">name</p>
	</div>
</div>
```

**Allows Multiple Arguments:** ✅ **YES**

### Examples

```html
<div strapi-collection="people">
    <div strapi-template="">
        <p strapi-field="name" strapi-class-add="color_class">name</p>
    </div>
</div>
```
Adds a class to the p element, with the class name given by the value in Strapi field color_class.

```html
<div strapi-collection="people">
    <div strapi-template="">
        <p strapi-field="name" strapi-class-add="color_class | text_decoration_class">name</p>
    </div>
</div>
```

Adds two classes to the p element, with the class names given by the values in Strapi fields color_class and text_decoration_class.