# strapi-class-replace

The `strapi-class-replace` attribute replaces an existing class on an element with a class with name specified by the value in a Strapi field. This works similarly to strapi-class-add but can be used to replace an existing placeholder class. The Strapify Conditional Expression Arguments section details the conditional expression syntax.

Below is the HTML to render a collection Person (plural people), with a `strapi-class-replace` attribute to add a class to the `p` element and remove the existing class black, with the replacement class decided by the value of the Strapi field color_class.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p
			class="black"strapi-field
			strapi-field="name"
			strapi-class-replace="color_class, black"
		>
			name
		</p>
	</div>
</div>
```

**Allows Multiple Arguments:** ✅ **YES**

### Examples

```html
<div strapi-collection="people">
    <div strapi-template="">
        <p
            class="black"
            strapi-field="name"
            strapi-class-replace="color_class, black"
        >
            name
        </p>
    </div>
</div>
```
Replaces the class black on the p element with a class which has its name stored in the Strapi field color_class.

```html
<div strapi-collection="people">
    <div strapi-template="">
        <p
            class="black bold"
            strapi-field="name"
            strapi-class-replace="color_class, black | text_decoration_class, bold"
        >
            name
        </p>
    </div>
</div>
```

Replaces the classes bold and black on the p element with classes which have their name stored in the Strapi fields text_decoration_class and color_class.