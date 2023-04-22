# strapi-class-conditional

This attribute will add a class to an element if the expression is true.  See the [Strapify Conditional Expression Arguments](../../notes/syntax-notes/strapify-conditional-expression-arguments.md) for more information on the syntax of the expression.

This attribute can be used as an alternative to `strapi-template-conditional` to conditionally style an element element based on the values of Strapi data.

**Allows Multiple Arguments:** ✅ YES

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

