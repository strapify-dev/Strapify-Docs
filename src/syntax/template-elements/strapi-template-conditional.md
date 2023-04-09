# strapi-template-conditional

The `strapi-template-conditional` attribute specifies that the element is a conditional template element. Conditional template elements function identically to standard template elements, but take a conditional expression argument which defines a condition that must be met by the data in a Strapi entry for this template to be used. The [Strapify Conditional Expression Arguments section](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md) details the conditional expression syntax. This attribute is useful in scenarios for which you want to have multiple templates so that certain entries can be rendered with a different appearance, or with different data displayed. A standard template element should always be included in the parent collection element as a fallback in the cases that the data for an entry in the collection does not pass any of the conditional expressions on the conditional template elements.

Below is the HTML to specify two template elements, which have different styles (from the classes red and green). A standard template is provided as a fallback in the case that none of the conditional templates have their conditions met.

```html
<div strapi-collection="people">
	<div class="red" strapi-template-conditional="is_employed == false">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>

	<div class="green" strapi-template-conditional="is_employed == true">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>

	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** 🚫 **NO**

**Examples**


    strapi-template-conditional="name == 'Paul Dirac'"

> | The template element will be used in the case the the person’s name is Paul Dirac. |
> | strapi-template-conditional | age < 90 | <div

    strapi-template-conditional="age < 90"

> | The template element will be used in the case the the person is less than 90 years old. |
> | strapi-template-conditional | is_employed == false | <div

    strapi-template-conditional="is_employed == false"

> | The template element will be used in the case the the person is not employed. |
> | strapi-template-conditional | name == 'Paul Dirac' && age == 82 | <div

    strapi-template-conditional="name == 'Paul Dirac' && age == 82"

> | The template element will be used in the case the the person’s name is Paul Dirac and their age is 82. |
> | strapi-template-conditional | (name == 'Paul Dirac' && age == 82) || is_employed == false | <div

    strapi-template-conditional="(name == 'Paul Dirac' && age == 82) || is_employed == false"

> | The template element will be used in the case the the person’s name is Paul Dirac and their age is 82 or if they’re unemployed. |
> | strapi-template-conditional | (name == 'Paul Dirac' && age == 82) || (is_employed == false && score == 3.0) | <div

    strapi-template-conditional="(name == 'Paul Dirac' && age == 82) || (is_employed == false && score == 3.0)"

> | The template element will be used in the case the the person’s name is Paul Dirac and their age is 82 or if they’re unemployed and their score is 3. |