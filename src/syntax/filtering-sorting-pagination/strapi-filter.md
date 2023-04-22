# strapi-filter

The `strapi-filter` attribute is used to specify a filter for the populated template elements in a collection element. The arguments for this attribute conform to the the [Strapi query string API parameter syntax](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/api-parameters.html), with the **_filter=_** prefix omitted (see examples). This allows for filtering to be done based on the value of the fields within a strapi entry. When multiple arguments are given they must be given a unique index and each must contain a logical operator to conform to the [Strapi query string API syntax for filtering](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/filtering-locale-publication.html#filtering).

Strapify will reflect changes to this attribute automatically if it is changed with a script.

Below is the HTML to render a collection called Person (plural people), filtered to only include people with an age of 42, with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-filter="[age][$eq]=42">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allows Multiple Arguments:** ✅ **YES**

### Examples

```html
<div 
    strapi-collection="people"
    strapi-filter="[name][$eq]=Paul Dirac"
>
```

The collection people will be filtered to include only people with the name Paul Dirac.

```html
<div 
    strapi-collection="people"
    strapi-filter="[$or][0][name][$eq]=Paul Dirac | [$or][1][name][$eq]=Richard Feynman"
>
```

The collection people will be filtered to include only people with the name Paul Dirac or Richard Feynman.

```html
<div 
    strapi-collection="people"
    strapi-filter="[$and][0][name][$eq]=Paul Dirac | [$and][1][age][$eq]=82"
>
```

The collection people will be filtered to include only people with the name Paul Dirac who are of age 82.

```html
<div 
    strapi-collection="people"
    strapi-filter="[$and][0][name][$eq]=Paul Dirac | [$and][1][age][$eq]=82 | [$and][2][name][$eq]=Richard Feynman"
>
```

The collection people will be filtered to include only people with the name Paul Dirac who are of age 82 and the name Richard Feynman.

```html
<div 
    strapi-collection="people"
    strapi-filter="[qs.fieldName][$eq]=qs.fieldValue"
>
```

The collection people will be filtered to include only people that meet the condition that the field name, given by the query string variable fieldName is equal to the the value given by the query string variable fieldValue. This is useful for creating dynamic pages that are populated with data from Strapi.