# strapi-single-type-class-conditional

The `strapi-single-type-class-conditional` attribute works much the same as the [strapi-class-conditional](../css-modifiers/strapi-class-conditional.md) attribute, but can be used on a single type element instead of a collection element.

This attribute will add a class to an element if the expression is true.  See the [Strapify Conditional Expression Arguments](../../notes/syntax-notes/strapify-conditional-expression-arguments.md) for more information on the syntax of the expression.

### Example

```html
<div strapi-collection="articles">
	<div strapi-template="">
		<div
			class="tag"
			strapi-class-conditional="type == 'nature', green | type == 'sports', red"
		>
			<p strapi-field="type">Tag name here.</p>
		</div>

		<p strapi-field="title">title goes here</p>
		<p strapi-field="author">author goes here</p>
	</div>
</div>
```
Adds the class green to the div element if the value of the Strapi field type is nature, and adds the class red to the div element if the value of the Strapi field type is sports.

Unlike the strapi-class-conditional attribute, does not need to exist as a child of a template element; it can exist anywhere.