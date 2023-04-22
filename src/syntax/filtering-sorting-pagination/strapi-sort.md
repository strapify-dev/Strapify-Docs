# strapi-sort

The `strapi-sort` attribute is used to specify a sort order for the populated template elements in a collection, relation or repeatable element. When multiple arguments are given, the sort is done in the order that the arguments appear.

Strapify will reflect changes to this attribute automatically if it is changed with a script.

The `strapi-sort-control` attribute can be used on buttons to control the behavior of the strapi-sort attribute when clicked.

---

Below is the HTML to render a collection called Person (people), sorted by the name field.
```html
<div strapi-collection="people" strapi-sort="name">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

---

**Allows Multiple Arguments:** ✅ **YES**

### Examples

```html
<div strapi-collection="people" strapi-sort="name">
```

The collection people will be sorted by name.

```html
<div strapi-collection="people" strapi-sort="name:asc">
```
The collection people will be sorted by name.

```html
<div strapi-collection="people" strapi-sort="id">
```
The collection people will be sorted by Strapi id.
```html
<div strapi-collection="people" strapi-sort="name:desc">
```
The collection people will be sorted by name, in descending order.
```html
<div strapi-collection="people" strapi-sort="name | age">
```
The collection people will be sorted by name then age.
```html
<div strapi-collection="people" strapi-sort="name | age | id">
```
The collection people will be sorted by name then age then id.
```html
<div strapi-collection="people" strapi-sort="qs.fieldName">
```
The collection people will be sorted by whatever field is stored in the query string parameter fieldName.
```html
<div strapi-collection="people" strapi-sort="[location][city]">
```
The collection people will be sorted by the value of city in the component field location.