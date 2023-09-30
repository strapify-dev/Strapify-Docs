# Strapify Docs

This documentation covers the Strapify system in detail with some HTML code examples. For a more beginner-friendly intro to Strapify, check out the [example tutorials](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Example%20Project%20-%20Jane%20Books%20Dog%20School%200fdcabadba004d73ad082d916c18688f.md), where we turn a static site into a Strapi CMS powered site.

[Example Project - Jane Books Dog School](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Example%20Project%20-%20Jane%20Books%20Dog%20School%200fdcabadba004d73ad082d916c18688f.md)

[9 Common Strapify Errors](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Example%20Project%20-%20Jane%20Books%20Dog%20School%200fdcabadba004d73ad082d916c18688f/9%20Common%20Strapify%20Errors%2025a6fef5eef24c73ac5ea3f3b15f646f.md)

## Overview

Strapify is like Tailwind or Bootstrap for the Strapi CMS. It is a script that implements common functionality for the population of websites with Strapi CMS data, abstracting it all away into simple to use custom data attributes.

The goal of the Strapify project is to enable the integration of a free open source CMS (Strapi) into an otherwise static website, without requiring additional code or otherwise complicating the development process. To this end, we seek compatibility and convenience for both manually built sites and those built with no-code website builders such as [Webflow](https://webflow.com/).

⬇️ [Download](https://strapify.s3.amazonaws.com/strapify-v0.0.7.js)

📂 Source Code (coming soon)

[Changelog and Known Issues](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Changelog%20and%20Known%20Issues%209e6dc6636b1a41a69591d2d8c70b5b10.md)

[Showcase](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Showcase%20af8ecfb660994b11a736c8433d79e10b.md)

### Quick Install (CDN)

```html
<script
	src="https://strapify.s3.amazonaws.com/strapify-v0.0.7.js"
	data-strapi-api-url="ENTER YOUR STRAPI URL HERE"
	type="text/javascript"
></script>
```

### Supported Strapi Field Types:

> ✅ Supported
> ⚠️ Work In Progress - do not use
> 🚫 Not Supported - do not use

<aside>
✅ Media
✅ images
✅ videos
🚫 audio
⚠️ files

</aside>

<aside>
✅ UID

</aside>

<aside>
✅ Email

</aside>

<aside>
⚠️ Password

</aside>

<aside>
✅ Relation

</aside>

<aside>
✅ Enumeration

</aside>

<aside>
🚫 JSON

</aside>

<aside>
🚫 Dynamic Zone

</aside>

<aside>
✅ Component

</aside>

<aside>
✅ Text

</aside>

<aside>
✅ Rich Text

</aside>

<aside>
✅ Date

</aside>

<aside>
✅ Boolean

</aside>

<aside>
✅ Number

</aside>

To request support for a strapi extension, plugin or feature, email [agoodman@civiconnect.ca](mailto:agoodman@civiconnect.ca).

### Supported Plugins:

- [Users & Permissions](https://docs.strapi.io/developer-docs/latest/plugins/users-permissions.html)
- [EZ Forms](https://market.strapi.io/plugins/strapi-plugin-ezforms)

### Reserved Keywords:

You must not use the following words as the names of Strapi collections, fields, components, etc…

- qs
- ls
- me
- true
- false
- undefined
- null

## Prerequisite Readings

You should have an understanding of the following concepts and technologies:

- [HTML family tree: descendants, ancestors, parents, children and siblings](http://web.simmons.edu/~grabiner/comm244/weekfour/document-tree.html)
- [HTML data attributes](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)
- [Query strings](https://www.positly.com/support/query-string-parameters/)
- [Strapi](https://docs.strapi.io/developer-docs/latest/getting-started/introduction.html#open-source-contribution)
- [Strapi query string API parameters](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/api-parameters.html)
- [Read the Strapify known issues](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Changelog%20and%20Known%20Issues%209e6dc6636b1a41a69591d2d8c70b5b10.md)

## Primary Elements



### Template Elements



### Collection Elements

_Collection elements_ are HTML elements that contain [template elements](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). These elements correspond to a Strapi collection. These elements will contain all the [populated template elements](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md) after Strapify executes*.* These elements are defined with the `[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` \*\*attribute. These elements may appear anywhere in the website, but may not exists as descendants of template elements.

**Allowed Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `strapi-sort` `strapi-filter` `strapi-page` `strapi-page-size` `strapi-hide-on-fail`

### Single Type Elements

_Single type elements_ are HTML elements that correspond to a Strapi single type field, Strapi single type relation or Strapi single type repeatable field (repeatable components and multiple media fields). These elements function much like [field elements](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md), relation elements or repeatable elements, except they do not correspond to any [collection element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). These elements are defined with the `strapi-single-type`, `strapi-single-type-relation` or `strapi-single-type-repeatable` attributes. How and which content of s*ingle type elements* are modified is contextual and depends on the element tag and the strapi field type being used. These elements may appear anywhere in the website, but may not exists as descendants of template elements.

**Allowed Attributes:**

`strapi-single-type` `strapi-single-type-into` `strapi-single-type-class-add` `strapi-single-type-class-replace` `strapi-single-type-class-conditional` `strapi-single-type-repeatable` `strapi-single-type-relation` `strapi-sort` `strapi-filter` `strapi-page` `strapi-page-size`

## Secondary Elements

### Relation Elements

_Relation elements_ are HTML elements that contain [template elements](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md) and belong to another [template element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). These elements work much like collection elements, but only inject Strapi data for each entry in the relation. Since relations belong to and entry in a Strapi collection, these elements must be descendants of a [template element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). These elements are defined with the `strapi-relation` attribute. Single type relations are also supported with `strapi-single-type-relation`, in which case will not be descendants of a [template element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md).

**Allowed Attributes:**

`strapi-relation` `strapi-single-type-relation` `strapi-sort` `strapi-filter` `strapi-page` `strapi-page-size` `strapi-hide-on-fail`

### Repeatable Elements (Media, Components)

_Repeatable elements_ are HTML elements that contain [template elements](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md) and belong to another [template element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). These elements work much like collection elements, but render data belonging to either a Strapi repeatable component or a Strapi multiple media type field. These elements are defined with the `strapi-repeatable` attribute or the `strapi-single-type-repeatable` attribute.

**Allowed Attributes:**

`strapi-repeatable` `strapi-single-type-repeatable` `strapi-sort` `strapi-filter` `strapi-page` `strapi-page-size` `strapi-hide-on-fail`

### Control Elements

_Control elements_ are HTML elements that can change the state of a parent collection element in response to user input. This allows for a collection to be rerendered with a new filter, sort or page. Control elements can take the form of a buttons, anchors, selects, radio buttons and check boxes. These elements will influence the closest ancestor collection element.

**Allowed Attributes:**

`strapi-page-control` `strapi-filter-control` `strapi-sort-control`

### State Elements (Error, Loading, Success)

State elements are HTML elements that can reflect the current state of the parent collection element. These element will be hidden or shown based on the state of the collection element. With these elements, the loading, failure and success states of a collection element can be displayed. These elements are defined with the `strapi-state-element` attribute. These elements respond to the state of the closest ancestor collection element.

**Allowed Attributes:**

`strapi-state-element`

## Strapify Element Summary

![This diagram summarizes the relationships between the essential Strapify element types and the attributes that are valid on each type. Excludes a few element types such as state elements and EZForms elements. ](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/strapify-element-diagram.png)

This diagram summarizes the relationships between the essential Strapify element types and the attributes that are valid on each type. Excludes a few element types such as state elements and EZForms elements.

## Attribute Value Syntax





--- syntax notes removed ---


## Custom Scripts & Events

Strapify can interface with other scripts through event listeners and HTML attribute mutations. Strapify will run after the `DOMContentLoaded` event has been emitted. This will ensure that any non async scripts will be executed before Strapify runs. If you would like a script to run before Strapify, but after the page has loaded, you should use a deferred script. If you would like a script to run after Strapify runs, you should wait for the `strapifyInitialized` event to be emitted on the document.

### Events

Below is an example of how to use the `strapifyInitialized` event.

```jsx
//emitted when strapify finishes rendering for the first time
//all Strapi data will have been rendered to the DOM before this event occurs
document.addEventListener("strapifyInitialized", (event) => {
	//you have access the authentication state and the user data if authenticated
	const userAuthenticated = event.detail.userAuthenticated;
	const userData = event.detail.user;

	//custom code that interacts with strapify...
	//or any custom code that requires that strapify has already rendered...
	//or any custom code that requires access to authenticated user information...
});
```

Below is an example of how to use the `strapiCollectionChange` event. This event is use on collection, relation and repeatable elements.

```jsx
//query select a collection element to which you would like to listen for changes
const peopleCollectionElement = document.querySelector("#people-collection");

//event emitted when the collection is rerendered or rendered for the first time
peopleCollectionElement.addEventListener(
	"strapifyCollectionChange",
	(event) => {
		//you have access to the collection element that changed and the collection data that was fetched.
		const collectionElement = event.target;
		const strapiCollectionData = event.detail.collectionData;

		//custom code...
	}
);
```

Below is an example of how to use the `strapiAuthRegistered` event.

```jsx
//query select an auth element to which you would like to listen for a successful registration
const formElement = document.querySelector("#register-form");

//event emitted when the user has submitted the form and the registration succeeded
formElement.addEventListener("strapiAuthRegistered", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```

Below is an example of how to use the `strapiAuthRegisterError` event.

```jsx
//query select an auth element to which you would like to listen for a failed registration
const formElement = document.querySelector("#register-form");

//event emitted when the user has submitted the form and the registration failed
formElement.addEventListener("strapiAuthRegisterError", (event) => {
	//you have access to the error message and the full javascript error
	const error = event.detail.error;
	const errorMessage = event.detail.errorMessage;

	//custom code...
});
```

Below is an example of how to use the `strapiAuthLoggedIn` event.

```jsx
//query select an auth element to which you would like to listen for a successful log in.
const formElement = document.querySelector("#login-form");

//event emitted when the user has submitted the login form and the log in succeeded
formElement.addEventListener("strapiAuthLoggedIn", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```

Below is an example of how to use the `strapiAuthLogInError` event.

```jsx
//query select an auth element to which you would like to listen for a failed log in.
const formElement = document.querySelector("#login-form");

//event emitted when the user has submitted the login form and the log in failed
formElement.addEventListener("strapiAuthLoggedIn", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```

Below is an example of how to use the `strapiUserAuthenticated` event.

```jsx
//event emitted when Strapify runs and validates existing user data from local storage
document.addEventListener("strapiUserAuthenticated", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```

Below is an example of how to use the `strapiUserAuthenticationError` event. When user data is found but could not be validated this event will fire. Currently, the invalid user data is just deleted and the page is reloaded immediately, so this event will never be used at the moment. An option to prevent an automatic page reload may be added in the future.

```jsx
//event emitted when Strapify runs and failed to validate existing user data
document.addEventListener("strapiUserAuthenticationError", (event) => {
	//custom code...
});
```

### Attribute Mutations

Some Strapify elements will automatically respond to changes made to their HTML attributes. When these mutations occur the collection will rerender using the new the attribute values. This allows custom scripts to change the filter, sort and page of collection elements, for example.

Elements that support attribute mutations:

- collection elements
- field elements
- relation elements
- repeatable elements
- single type field elements

Below is an example of how to mutate a the strapi-filter-control of a Strapify collection.

```jsx
//query select a collection element so we can change its strapi-filter-control value
const collectionElement = document.querySelector("#people-collection");

//simply set the new attribute value and Strapify will respond automatically
collectionElement.setAttribute("strapi-filter", "[name][$eq]=Austin");
```

## Syntax

### strapi-collection

The `strapi-collection` attribute specifies that the element is a [collection element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md). \*\*The value of this attribute is the pluralized name of a Strapi collection. Strapify will search the element for a template element or a set of template elements if there are conditional template elements, and duplicate it/them for each entry in the collection.

If multiple template elements exist as children to the collection element, the first occurring template element will be used. If there are two conditional template elements with equivalent conditions, existing as children to the collection element, the first occurrence will be used. All template elements will be removed from the DOM when Strapify runs (you can have many copies of your template to help visualize how your site will look during development, Strapify will remove them for you). Any elements existing as children to the collection element that is not a template element, will be left untouched (you can put text, links, buttons or other things within collection elements without causing problems for Strapify).

If the collection element contains a standard template in addition to conditional template elements, any Strapi entries that don’t meet the conditions for any of the conditional templates, will use the standard template.

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

---

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-sort](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-filter](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page-size](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-hide-on-fail](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name              | Value                            | HTML                                                       | Description                                                                                                                                                                                                    |
| ----------------- | -------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| strapi-collection | my_strapi_collection_name_plural | <div strapi-collection="my_strapi_collection_name_plural"> | Mark the div element as a collection element for the Strapi collection named my_strapi_collection_name_plural.                                                                                                 |
| strapi-collection | people                           | <div strapi-collection="people">                           | Mark the div element as a collection element for the Strapi collection named people.                                                                                                                           |
| strapi-collection | qs.collectionName                | <div strapi-collection="qs.collectionName">                | Mark the div element as a collection element for the Strapi collection with name stored in the current page’s query string variable collectionName. E.g. www.website.com?collectionName=strapi_collection_name |

### strapi-sort

The `strapi-sort` attribute is used to specify a sort order for the populated template elements in a collection, relation or repeatable element. The arguments for this attribute conform to the the [Strapi query string API parameter syntax](https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest/api-parameters.html), with the `filters` prefix omitted (see examples). This allows for sorting to be done based on the value of the fields within a Strapi entry. When multiple arguments are given, the sort is done in the order that the arguments appear.

Strapify will reflect changes to this attribute automatically if it is changed with a script.

---

Below is the HTML to render a collection called Person (people), sorted by the name field, with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-sort="name">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

---

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-relation](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-repeatable](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-sort-control](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name        | Value            | HTML                                                            | Description                                                                                               |
| ----------- | ---------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------ | ---- | -------------------------------------------------------------- |
| strapi-sort | name             | <div strapi-collection="people" strapi-sort="name">             | The collection people will be sorted by name.                                                             |
| strapi-sort | name:asc         | <div strapi-collection="people" strapi-sort="name:asc">         | The collection people will be sorted by name.                                                             |
| strapi-sort | id               | <div strapi-collection="people" strapi-sort="id">               | The collection people will be sorted by Strapi id.                                                        |
| strapi-sort | name:desc        | <div strapi-collection="people" strapi-sort="name:desc">        | The collection people will be sorted by name, in descending order.                                        |
| strapi-sort | name             | age                                                             | <div strapi-collection="people" strapi-sort="name                                                         | age">                                             | The collection people will be sorted by name then age. |
| strapi-sort | name             | age                                                             | id                                                                                                        | <div strapi-collection="people" strapi-sort="name | age                                                    | id"> | The collection people will be sorted by name then age then id. |
| strapi-sort | qs.fieldName     | <div strapi-collection="people" strapi-sort="qs.fieldName">     | The collection people will be sorted by whatever field is stored in the query string parameter fieldName. |
| strapi-sort | [location][city] | <div strapi-collection="people" strapi-sort="[location][city]"> | The collection people will be sorted by the value of city in the component field location.                |

### strapi-filter

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

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-relation](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-repeatable](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` strapi-filter-control

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name          | Value                  | HTML | Description |
| ------------- | ---------------------- | ---- | ----------- |
| strapi-filter | [name][$eq]=Paul Dirac | <div |

    strapi-collection="people"
    strapi-filter="[name][$eq]=Paul Dirac"

> | The collection people will be filtered to include only people with the name Paul Dirac. |
> | strapi-filter | [$or][0][name][$eq]=Paul Dirac |
> [$or][1][name][$eq]=Richard Feynman | <div

    strapi-collection="people"
    strapi-filter="[$or][0][name][$eq]=Paul Dirac | [$or][1][name][$eq]=Richard Feynman"

> | The collection people will be filtered to include only people with the name Paul Dirac or Richard Feynman |
> | strapi-filter | [$and][0][name][$eq]=Paul Dirac |
> [$and][1][age][$eq]=82 | <div

    strapi-collection="people"
    strapi-filter="[$and][0][name][$eq]=Paul Dirac | [$and][1][age][$eq]=82"

> | The collection people will be filtered to include only people with the name Paul Dirac who are of age 82. |
> | strapi-filter | [qs.fieldName][$eq]=qs.fieldValue | <div

    strapi-collection="people"
    strapi-filter="[qs.fieldName][$eq]=qs.fieldValue"

> | The collection people will be filtered to include only people that meet the condition that the field name, given by the query string variable fieldName is equal to the the value given by the query string variable fieldValue. |
> | TODO: component example | | | |

### strapi-page

The `strapi-page` attribute is used to specify a which page Strapify will fetch from Strapi. The default value is 1. When an out of bounds page index is given, Strapify will automatically convert it to the nearest valid index.

Strapify will reflect changes to this attribute automatically if it is changed with a script.

Below is the HTML to render the second page of the collection Person (plural people), with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-page="2">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-relation](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-repeatable](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name        | Value | HTML                                             | Description                                                  |
| ----------- | ----- | ------------------------------------------------ | ------------------------------------------------------------ |
| strapi-page | 1     | <div strapi-collection="people" strapi-page="1"> | Strapify will render the first page of the collection People |

### strapi-page-size

The `strapi-page-size` attribute is used to specify the size of pages when data is fetched from Strapi. When unspecified Strapi’s default size will be used.

Strapify will reflect changes to this attribute automatically if it is changed with a script.

Below is the HTML to render a collection called Person (plural people), with a page size of 5, with the name and age fields to be rendered into `p` elements.

```html
<div strapi-collection="people" strapi-page="1" strapi-page-size="5">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-relation](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-repeatable](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name             | Value | HTML                                                   | Description                                                                     |
| ---------------- | ----- | ------------------------------------------------------ | ------------------------------------------------------------------------------- |
| strapi-page-size | 25    | <div strapi-collection="people" strapi-page-size="25"> | Strapify will render the first page of the collection People with page size 25. |

### strapi-hide-on-fail

The `strapi-hide-on-fail` attribute will cause a collection element, relation element or repeatable element to be hidden in the case that an error occurred when fetching data. This attribute is useful in scenarios for which failure is expected, such as when the collection is only available to authenticated users but the current user has not yet authenticated. It may also be used to hide data if there is an unexpected error, but state elements should be preferred in such cases.

Strapify currently accomplishes this by adding a class with CSS attribute `display: none;` on the element. It will not work if you have specified the CSS display attribute inline or with !important.

Below is the HTML to hide a collection in the case that there is an error retrieving the collection data.

```html
<div strapi-collection="people" strapi-hide-on-fail="">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-relation](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-repeatable](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                | Value | HTML                                                    | Description                                                                                                |
| ------------------- | ----- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| strapi-hide-on-fail | N/A   | <div strapi-collection="people" strapi-hide-on-fail=""> | Strapify will attempt to render the collection People. If an error occurs, the element will become hidden. |

---

### strapi-template

The `strapi-template` attribute specifies that the element is a template element. Template elements must exist as children of collection elements, relation elements or repeatable elements. *S*trapify will search the element for child field elements, relation elements and repeatable elements. If multiple template elements exist as children to a collection element, relation element or repeatable element, the first occurring template element will be used. All template elements will be removed from the DOM when Strapify runs. If a collection element, relation element or repeatable element contains a standard template in addition to conditional template elements, any Strapi entries that don’t meet the conditions for any of the conditional templates, will use the standard template as a fallback.

Below is the HTML to specify a template element for the collection people, with two `p` elements to render the name and age fields.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-template-conditional](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name            | Value | HTML                     | Description                                                                                                    |
| --------------- | ----- | ------------------------ | -------------------------------------------------------------------------------------------------------------- |
| strapi-template | N/A   | <div strapi-template=""> | Mark the div element as a collection element for the Strapi collection named my_strapi_collection_name_plural. |

### strapi-template-conditional

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

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-template](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                        | Value                | HTML | Description |
| --------------------------- | -------------------- | ---- | ----------- |
| strapi-template-conditional | name == 'Paul Dirac' | <div |

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

---

### strapi-relation

The `strapi-relation` attribute specifies that the element is a relation element. Relation elements function identically to collection elements, except they are automatically filtered to only retrieve entries in the collection in the relation. Like collection elements, relation elements must contain templates. The field elements in those templates will reference fields existing on entries of the related collection. The argument must provide both the name of the relation field and the name of the collection being related, separated by a comma.

Below is the HTML to render the collection people, which has a relation with itself to define each person’s children. Each child of a person will have their name and age rendered.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>

		<div strapi-relation="children, people">
			<div strapi-template="">
				<p strapi-field="name">child name goes here</p>
				<p strapi-field="age">child age goes here</p>
			</div>
		</div>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-sort](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-filter](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page-size](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-hide-on-fail](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name            | Value            | HTML                                     | Description                                                                                                                   |
| --------------- | ---------------- | ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| strapi-relation | children, people | <div strapi-relation="children, people"> | Marks the div element as a relation element with the relation defined in the field children for the collection called people. |
| strapi-relation | pets, animals    | <div strapi-relation="pets, animals">    | Marks the div element as a relation element with the relation defined in the field pets for the collection called animals.    |

### strapi-repeatable

The `strapi-repeatable` attribute specifies that the element is a repeatable element. Repeatable elements function identically to collection elements, except their data is not pulled from a strapi collection but rather the data in a collection entries field. This attribute is used to render either multi-media fields (multiple images, multiple videos, …) or repeatable components. Like collection elements, repeatable elements must contain templates. The field elements in those templates must use the name of you repeatable field (see below).

Below is the HTML to render the collection people, with a multiple media field of images called my_images.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name goes here</p>
		<p strapi-field="age">age goes here</p>

		<div strapi-repeatable="my_images">
			<div strapi-template="">
				<img strapi-field="my_images" />
			</div>
		</div>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-sort](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-filter](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page-size](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-hide-on-fail](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name | Value | HTML | Description |
| ---- | ----- | ---- | ----------- |
|      |       |      |             |

---

### strapi-field


### strapi-into



### strapi-class-add

The `strapi-class-add` attribute adds a class to an element with the name specified by the value in a Strapi field. These elements must exist as children of a template element. This allows the styling of elements to be changed through the Strapi CMS.

Below is the HTML to render a collection Person (plural people), with a `strapi-class-add` attribute to add a class to the `p` element, with the class decided by the value of the Strapi field color_class.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name" strapi-class-add="color_class">name</p>
	</div>
</div>
```

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-field](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name             | Value       | HTML                                                   | Description                                                                                        |
| ---------------- | ----------- | ------------------------------------------------------ | -------------------------------------------------------------------------------------------------- | ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| strapi-class-add | color_class | <p strapi-field="name" strapi-class-add="color_class"> | Adds a class to the p element, with the class name given by the value in Strapi field color_class. |
| strapi-class-add | color_class | text_decoration_class                                  | <p strapi-field="name" strapi-class-add="color_class                                               | text_decoration_class"> | Adds two classes to the p element, with the class names given by the values in Strapi fields color_class and text_decoration_class. |

### strapi-class-replace

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

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-field](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name                 | Value              | HTML                                                                            | Description                                                                                                       |
| -------------------- | ------------------ | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| strapi-class-replace | color_class, black | <p class="black" strapi-field="name" strapi-class-replace="color_class, black"> | Replaces the class black on the p element with a class which has its name stored in the Strapi field color_class. |
| strapi-class-replace | color_class, black | text_decoration_class, bold                                                     | <p                                                                                                                |

    class="black bold"
    strapi-field="name"
    strapi-class-replace="color_class, black | text_decoration_class, bold"

> | Replaces the classes bold and black on the p element with classes which have their name stored in the Strapi fields text_decoration_class and color_class. |

### strapi-class-conditional

The `strapi-class-conditional` attribute adds a class to an element only in the case that the given conditional expression evaluates to true. This attribute can be used as an alternative to `strapi-template-conditional` to conditionally style an element element based on the values of Strapi data.

Below is the HTML to specify classes to be conditionally added to the div element with the strapi-class-conditional attribute. If the article type is nature, the tag is green. If the article type is sports, the tag is red.

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

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-field](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** ✅ YES

**Examples:**

| Name | Value | HTML | Description |
| ---- | ----- | ---- | ----------- |
|      |       |      |             |

---

### strapi-single-type

The `strapi-single-type` attribute works much the same as `strapi-field`, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the value of a Strapi single type field to be rendered in the element.

| Strapi Field Type | HTML Elements | Comments                                                                                                                                                                               |
| ----------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Text              | p h span div  | The div is typically invalid but can be used as a special case to embed a video. For it to work, your text field must contain a link and the div must contain an iframe child element. |
| Email             | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Rich Text         | div           | HTML elements will be created in the div to render the rich text.                                                                                                                      |
| Number            | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Enumeration       | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Date              | p h span      | Field data will be inserted as text content.                                                                                                                                           |
| Media (Image)     | img           | The image source will be set to point to the Strapi url for the image.                                                                                                                 |
| Media (Video)     | div           | A video element will be inserted into the div.                                                                                                                                         |
| Boolean           | p h span      | Field data will be inserted as text content.                                                                                                                                           |

Below is the HTML to render a few fields from the single type collection info.

```html
<div>
	<h1 strapi-single-type="info.company_name">Company Name</h1>
	<img strapi-single-type="info.company_image" />
	<div strapi-single-type="info.bio">
		<p>placeholder for bio<p>
	</div>
</div
```

**Allowed Elements:**

`div` `p` `h` `span` `img`

**Related Attributes:**

`[strapi-template](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-template-conditional](https://www.notion.so/Using-Custom-JavaScript-to-Extend-Strapify-d8a3553264b143e8b45188285778514e)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name               | Value                   | HTML                                             | Description                                                                                                                          |
| ------------------ | ----------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| strapi-single-type | info.name               | <p strapi-single-type="info.name">               | Renders the value in the Strapi single type field name for the single type collection info.                                          |
| strapi-single-type | home_page.title         | <p strapi-single-type="home_page.title">         | Renders the value in the Strapi single type field title for the single type collection home_page.                                    |
| strapi-single-type | home_page.article.title | <p strapi-single-type="home_page.article.title"> | Renders the value in title, which is an element of a component called article which belongs to the home_page single type collection. |

### strapi-single-type-into

The `strapi-single-type-into` attribute is used to pass data from a Strapi single type collection field directly into an HTML attribute.

Below is the HTML to set the alt text of the `img` element to the value held in the Strapi single type field `alt_text`.

```html
<img
	strapi-single-type-field="info.company_image"
	strapi-into="info.company_image_alt_text -> alt"
/>
```

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-single-type-field](https://www.notion.so/Adding-Filters-to-a-Collection-Using-Strapify-d79e674e302842169c3a3808ea4564f3)`

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name                                                | Value                                                                                                                                                                                                                   | HTML                                                   | Description                                                                                                             |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| strapi-single-type-into                             | info.company_image_alt_text -> alt                                                                                                                                                                                      | <img strapi-into="info.company_image_alt_text -> alt"> | Sets the alt attribute of the img element to the value in the strapi single type field alt_text of the collection info. |
| strapi-single-type-into                             | home_page.element_id -> id                                                                                                                                                                                              | home_page.alt_text -> alt                              | <img                                                                                                                    |
| strapi-single-type-into="home_page.element_id -> id | home_page.alt_text -> alt"                                                                                                                                                                                              |
| >                                                   | Sets the id of the img element to the value in the Strapi single type field element_id and sets the alt attribute of the img element to the value in the Strapi single type field alt_text of the collection home_page. |

### strapi-single-type-class-add

The `strapi-single-type-class-add` attribute works much the same as `strapi-class-add` attribute, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the value of a Strapi single type field to be added to an element’s class list.

Below is the HTML to render a the Strapi single type field company_name of the single type collection info. The `strapi-single-type-class-add` attribute causes the value of the field company_name_color_class from the info collection to be added to the `h1` element’s class list.

```html
<h1
	strapi-single-type-field="info.company_name"
	strapi-class-add="info.company_name_color_class"
>
	company name
</h1>
```

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-single-type-field](https://www.notion.so/Adding-Filters-to-a-Collection-Using-Strapify-d79e674e302842169c3a3808ea4564f3)`

**Allows Multiple Arguments:** ✅ **YES**

**Examples:**

| Name                         | Value       | HTML                                                                                 | Description                                                                                                            |
| ---------------------------- | ----------- | ------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| strapi-single-type-class-add | color_class | <p strapi-field="name" strapi-single-type-class-add="info.company_name_color_class"> | The value of the field company_name_color_class from the info collection will be added to the h1 element’s class list. |

### strapi-single-type-class-replace

The `strapi-single-type-class-add` attribute works much the same as `strapi-class-add` attribute, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the value of a Strapi single type field to be added to an element’s class list, replacing an the specified existing class.

```html
<h1
	strapi-single-type-field="info.company_name"
	strapi-class-replace="info.company_name_color_class, black"
>
	company name
</h1>
```

### strapi-single-type-class-conditional

The `strapi-single-type-class-conditional` attribute works much the same as `strapi-class-conditional` attribute, but does not need to exist as a child of a template element; it can exist anywhere. Instead, this attribute will cause the class name value to be added to an element’s class list, given that the specified condition is met.

### strapi-single-type-relation

The `strapi-single-type-relation` attribute works much the same as the `strapi-relation` attribute, but does not need to exist as a child of a template element; it can exist anywhere.

Below is the HTML to render the single type field employees which belongs to the Company single type. The employees field is a relation with the collection Person (people).

```html
<div strapi-single-type-relation="Company.employees, people">
	<div strapi-template="">
		<p strapi-field="name">employee name goes here</p>
		<p strapi-field="age">employee age goes here</p>
	</div>
</div>
```

**Allowed Elements:**

`div`

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-sort](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-filter](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-page-size](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-hide-on-fail](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                        | Value                     | HTML                                              | Description                                                                                                                                                                             |
| --------------------------- | ------------------------- | ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| strapi-single-type-relation | Company.employees, people | <div strapi-relation="Company.employees, people"> | Marks the div element as a relation element with the relation defined in the field employees for the single type called Company. The relation with with the Person (people) collection. |

### strapi-single-type-repeatable

The `strapi-single-type-repeatable` attribute works much the same as the `strapi-repeatable` attribute, but does not need to exist as a child of a template element; it can exist anywhere.

---

### strapi-auth

`strapi-auth` is the first attribute that should be added to a login or register form when configuring the Strapify authentication system.

The basic authentication system for Strapify consists of three parts:

1. The `strapi-auth` attribute, which can be set to either "authenticate" or "register" to indicate the form's purpose.
2. The `strapi-auth-input` attribute, which can be set to the Strapi data field. For login, the keyword "identifier" is reserved for the username. For registration, the attribute can be set to the field names such as "username", "email", "password" etc.
3. The `strapi-auth-submit` attribute, which submits the form when clicked.

The Strapify auth system is intended for use on simple projects and it’s primary use is to show or hide Strapi collections depending on whether the user is logged in.

**\*\***Note - If working with highly sensitive data or on projects that require any level of complexity beyond showing/hiding collections, the Strapify auth system is not recommended.**\*\***

Example of a login form:

```html
<form strapi-auth="authenticate">
	<label for="username">Username</label>
	<input
		type="text"
		placeholder="Enter Username"
		name="username"
		strapi-auth-input="identifier"
		required
	/>

	<label for="psw">Password</label>
	<input
		type="password"
		placeholder="Enter Password"
		name="psw"
		strapi-auth-input="password"
		required
	/>

	<button type="submit" strapi-auth-submit>Login</button>
</form>
```

Example of a registration form:

```html
<form strapi-auth="register">
	<label for="username">Username</label>
	<input
		type="text"
		placeholder="Enter Username"
		name="username"
		strapi-auth-input="username"
		required
	/>

	<label for="email">Email</label>
	<input
		type="text"
		placeholder="Enter Email"
		name="email"
		strapi-auth-input="email"
		required
	/>

	<label for="psw">Password</label>
	<input
		type="password"
		placeholder="Enter Password"
		name="psw"
		strapi-auth-input="password"
		required
	/>

	<button type="submit" strapi-auth-submit>Register</button>
</form>
```

Note: Make sure to use the correct field names corresponding to the fields in your Strapi user model.

---

**Allowed Elements:**

`form`

**Related Attributes:**

`[strapi-auth-input](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name        | Value        | HTML                          | Description                                                                                              |
| ----------- | ------------ | ----------------------------- | -------------------------------------------------------------------------------------------------------- |
| strapi-auth | authenticate | <form strapi-auth="register"> | Marks the form element as a form that should authenticate users using the Strapify authentication system |
| strapi-auth | register     | <form strapi-auth="register"> | Marks the form element as a form that should register users using the Strapify authentication system     |

### strapi-auth-input

`strapi-auth-input` is used inside a form where the `strapi-auth` attribute is being used. The `strapi-auth-input` attribute is used to specify the Strapi user field that the input element is associated with. The attribute value should match the field name in the Strapi user model. For example, in a registration form, the input element for the username field would have `strapi-auth-input="username"`, and the input element for the email field would have `strapi-auth-input="email"`.

When used in a login form, the `strapi-auth-input` attribute should be set to "identifier" to specify the username field.

---

Note that if you have one input field that you’d like applied to more than one Strapi user data field, you can use multiple arguments to accomplish this like so:

By far the most common use case for this is during registration, when one input field should submit it’s value as the new user’s username and email

```html
<form strapi-auth="register">
	<label for="email">Email</label>
	<input
		type="email"
		placeholder="Enter Email"
		name="email"
		strapi-auth-input="username | email"
		required
	/>

	<label for="psw">Password</label>
	<input
		type="password"
		placeholder="Enter Password"
		name="psw"
		strapi-auth-input="password"
		required
	/>

	<button type="submit" strapi-auth-submit>Login</button>
</form>
```

---

**Allowed Elements:**

`input`

**Related Attributes:**

`[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** ✅ YES

**Examples:**

| Name              | Value      | HTML                                                                 | Description                                                                                        |
| ----------------- | ---------- | -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| strapi-auth-input | identifier | <input type="text" name="username" strapi-auth-input="identifier" /> | Marks the username input as the identifier used for authentication (login).                        |
| strapi-auth-input | username   | <input type="text" name="username" strapi-auth-input="username">     | Another username input, however this would be used for registration to set the new user’s username |
| strapi-auth-input | username   | email                                                                | <input type="text" name="username" strapi-auth-input="username                                     | email"> | Another username input, however this would be used for registration to set the new user’s username and email to the value entered in the username input. |

### strapi-auth-submit

The `strapi-auth-submit`attribute should be used in `strapi-auth` forms to indicate the submit button. When clicked, it triggers the authentication process (either registration or login). The attribute is typically added to a <button> element of type "submit".

If `strapi-auth` is set to `register`, the form will attempt to create a new user from the credentials provided in the form inputs using `strapi-auth-input`.

If `strapi-auth` is set to `authenticate`, it will attempt to authenticate the user based on the credentials provided in the login form, and the user’s JWT token will be stored in localStorage.

---

**Allowed Elements:**

`button`

**Related Attributes:**

`[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-input](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

See code example in `strapi-auth`

### strapi-success-redirect

The `strapi-success-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form is successfully submitted. It should be added on the <form> component itself.

---

**Allowed Elements:**

`form`

**Related Attributes:**

`[strapi-ezforms-form](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-ezforms-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                    | Value | HTML                                                           | Description                                                                         |
| ----------------------- | ----- | -------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| strapi-success-redirect | /     | <form strapi-ezforms-form strapi-success-redirect="/thankyou"> | Redirects the user to the “thank you” page when the form is successfully submitted. |

### strapi-error-redirect

The `strapi-error-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form fails to submit. It should be added on the <form> component itself.

---

**Allowed Elements:**

`form`

**Related Attributes:**

`[strapi-ezforms-form](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-ezforms-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Example%20Project%20-%20Jane%20Books%20Dog%20School%200fdcabadba004d73ad082d916c18688f/User%20Authentication%20with%20Strapify%200620d66a1c5e4df5aef0b5adbb4cb519.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                  | Value | HTML                                                        | Description                                                                   |
| --------------------- | ----- | ----------------------------------------------------------- | ----------------------------------------------------------------------------- |
| strapi-error-redirect | /     | <form strapi-ezforms-form strapi-success-redirect="/error"> | Redirects the user to the error page when the form submission is unsuccessful |

### strapi-logout

When set on a <button> element, the `strapi-logout` attribute will log out the user when the button is clicked. It can be used together with `strapi-logout-redirect` to destroy the token and redirect the user to another page.

---

**Allowed Elements:**

`button`

**Related Attributes:**

`[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name          | Value | HTML                                   | Description                                  |
| ------------- | ----- | -------------------------------------- | -------------------------------------------- |
| strapi-logout | N/A   | <button strapi-logout>Log Out</button> | Logs the user out when the button is pressed |

### strapi-logout-redirect

The `strapi-logout-redirect` attribute can be used on a `strapi-logout` element to redirect a user to a different URL when the element is clicked.

---

**Allowed Elements:**

`button`

**Related Attributes:**

`[strapi-auth](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-auth-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-logout](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                   | Value | HTML                                                              | Description                                                                     |
| ---------------------- | ----- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| strapi-logout-redirect | /     | <button strapi-logout strapi-logout-redirect="/">Log Out</button> | Logs the user out and redirects to the landing page when the button is pressed. |

### strapi-ezforms-form

The `strapi-ezforms-form` attributes is used on form elements to identify the form as one which will submit form data to the EZForms plugin endpoints in Strapi.

The [strapi EZForms plugin](https://market.strapi.io/plugins/strapi-plugin-ezforms) will have to be installed and configured. Here’s a [full tutorial](https://www.notion.so/Using-Strapify-to-Handle-Form-Submissions-with-EZForms-04dfb69ea83b4e49ab471549d8672487)

When submitted, it emits two custom events: `strapiEZFormsSubmitted` and `strapiEZFormsError`. These events can be used to trigger UI changes or other custom logic on form submission.

There are two other simple ways to trigger UI changes on form submission.

1. You can set `strapi-state-element` on an element to show/hide elements depending on the state of the form submission. The two key values would be `strapi-state-element="success"`, to be set on the element you’d like to show when the user successfully submits the form, and `strapi-state-element="error"`, to be set on the element you’d like to show when the form submission fails.
2. You can use `strapi-success-redirect` or `strapi-error-redirect` to redirect to a different URL when a form submission succeeds or fails.

Below is the HTML to configure a form with `strapi-ezforms-form`

```html
<form strapi-ezforms-form>
	<label for="username">Email</label>
	<input type="email" placeholder="Enter Email" name="email" required />

	<label for="message">Your Message</label>
	<input type="password" placeholder="Enter Password" name="psw" required />

	<button type="submit" strapi-ezforms-submit>Submit</button>
</form>
```

Strapify automatically parses all of the form’s input fields.

---

**Allowed Elements:**

`form`

**Related Attributes:**

`[strapi-ezforms-submit](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

See code example above

### strapi-ezforms-submit

The `strapi-ezforms-submit` attribute should be used in `strapi-ezforms-form` forms to indicate the submit button. When clicked, it triggers the form submission process. The attribute is typically added to a <button> element of type "submit".

---

**Allowed Elements:**

`button`

**Related Attributes:**

`[strapi-ezforms-form](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-error-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-success-redirect](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)` `[strapi-state-element](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94/Example%20Project%20-%20Jane%20Books%20Dog%20School%200fdcabadba004d73ad082d916c18688f/User%20Authentication%20with%20Strapify%200620d66a1c5e4df5aef0b5adbb4cb519.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

See code example in `strapi-ezforms`

### strapi-page-control

The `strapi-page-control` attribute is used on input elements, such as buttons, radio buttons and selects. This attribute accepts either a number, which will directly set the page of the collection element, or a sign prefixed number which will increment/decrement that page by the number that follows.

Below is the HTML to paginate and render render a collection Person (people), with a button to go to the first page, next page and previous page.

```html
<div strapi-collection="people" strapi-page="1" strapi-page-size="4">
	<a strapi-page-control="1">First Page</a>
	<a strapi-page-control="+1">Next Page</a>
	<a strapi-page-control="-1">Prev Page</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to paginate and render render a collection Person (people), with a select option for the first four pages.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use select elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- this way will work with webflow (using value) -->
			<select strapi-page-control="">
				<option value="1">1</option>
				<option value="2">2</option>
				<option value="3">3</option>
				<option value="4">4</option>
			</select>

			<!-- this is the second way (using strapi-control-value) -->
			<select strapi-page-control="">
				<option strapi-control-value="1">1</option>
				<option strapi-control-value="2">2</option>
				<option strapi-control-value="3">3</option>
				<option strapi-control-value="4">4</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to paginate and render render a collection Person (people), with a radio button for the first two pages.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use radio type input elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- this way will work with webflow (using value) -->
			<div strapi-page-control="">
				<label> <input type="radio" name="radio" value="1" /> Paul </label>
				<label> <input type="radio" name="radio" value="2" /> Richard </label>
			</div>

			<!-- this is the second way (using strapi-control-value) -->
			<div strapi-page-control="">
				<label>
					<input type="radio" name="radio" strapi-control-value="1" /> Paul
				</label>
				<label>
					<input type="radio" name="radio" strapi-control-value="2" /> Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

**Allowed Elements:**

`a` `button` `select` `input type="radio"` `input type="checkbox"`

**Related Attributes:**

`[strapi-page](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                 | Value   | HTML                               | Description                                                                                                    |
| -------------------- | ------- | ---------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| strapi-state-element | loading | <p strapi-state-element="loading"> | The p element is displayed only when the parent collection element is loading the Strapi data.                 |
| strapi-state-element | success | <p strapi-state-element="success"> | The p element is displayed only when the parent collection element has loaded the data and finished rendering. |
| strapi-state-element | error   | <p strapi-state-element="error">   | The p element is displayed only when the parent collection element has failed to retrieve the Strapi data.     |

### strapi-filter-control

The `strapi-filter-control` attribute is used on input elements, such as buttons, radio buttons, selects and check boxes. When the input element triggers an event, the value of the attribute will set the value of `strapi-filter` on the parent collection element, and the collection will be rerendered with the new filter. The value of this attribute will be the new value of `strapi-filter` on the parent collection when the input event is triggered.

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two possible `a` elements is clicked.

```html
<div strapi-collection="people">
	<a strapi-filter-control="[first_name][$eq]=Paul">Filter by Paul</a>
	<a strapi-filter-control="[first_name][$eq]=Richard">Filter by Richard</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two options in a `select` is chosen.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use select elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- this way will work with webflow (using value) -->
			<select strapi-filter-control="">
				<option value="[first_name][$eq]=Paul">Paul</option>
				<option value="[first_name][$eq]=Richard">Richard</option>
			</select>

			<!-- this is the second way (using strapi-control-value) -->
			<select strapi-filter-control="">
				<option strapi-control-value="[first_name][$eq]=Paul">Paul</option>
				<option strapi-control-value="[first_name][$eq]=Richard">
					Richard
				</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two `radio` buttons is clicked.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use radio type input elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- this way will work with webflow (using value) -->
			<div strapi-filter-control="">
				<label>
					<input type="radio" name="radio" value="[first_name][$eq]=Paul" />
					Paul
				</label>
				<label>
					<input type="radio" name="radio" value="[first_name][$eq]=Richard" />
					Richard
				</label>
			</div>

			<!-- this is the second way (using strapi-control-value) -->
			<div strapi-filter-control="">
				<label>
					<input
						type="radio"
						name="radio"
						strapi-control-value="[first_name][$eq]=Paul"
					/>
					Paul
				</label>
				<label>
					<input
						type="radio"
						name="radio"
						strapi-control-value="[first_name][$eq]=Richard"
					/>
					Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), filtered by the first names Paul and/or Richard depending on whether or not the corresponding checkbox type `input` elements is selected. Since both checkboxes can be selected at once, the logical `[$or]` Strapi operator is used.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use checkbox type input elements in webflow -->
		<form>
			<!-- you must use strapi-control-value for checkboxes -->
			<div strapi-filter-control="">
				<label>
					<input
						type="checkbox"
						strapi-control-value="[$or][0][first_name][$eq]=Paul"
					/>
					Paul
				</label>
				<label>
					<input
						type="checkbox"
						strapi-control-value="[$or][1][first_name][$eq]=Richard"
					/>
					Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

**Related Attributes:**

`[strapi-filter](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

### strapi-sort-control

The `strapi-sort-control` attribute is used on input elements, such as buttons, radio buttons, selects and check boxes. When the input element triggers an event, the value of the attribute will set the value of `strapi-sort` on the parent collection element, and the collection will be rerendered with the new sort. The value of this attribute will be the new value of `strapi-sort` on the parent collection when the input event is triggered.

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of the `a` elements is clicked.

```html
<div strapi-collection="people">
	<a strapi-sort-control="first_name">Filter by name</a>
	<a strapi-sort-control="age">Filter by age</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of two options in a `select` is chosen.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use select elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- this way will work with webflow (using value) -->
			<select strapi-sort-control="">
				<option value="first_name">Paul</option>
				<option value="age">Richard</option>
			</select>

			<!-- this is the second way (using strapi-control-value) -->
			<select strapi-sort-control="">
				<option strapi-control-value="first_name">Paul</option>
				<option strapi-control-value="age">Richard</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of two `radio` buttons is clicked.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use radio type input elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- this way will work with webflow (using value) -->
			<div strapi-sort-control="">
				<label>
					<input type="radio" name="radio" value="first_name" /> Paul
				</label>
				<label> <input type="radio" name="radio" value="age" /> Richard </label>
			</div>

			<!-- this is the second way (using strapi-control-value) -->
			<div strapi-sort-control="">
				<label>
					<input type="radio" name="radio" strapi-control-value="first_name" />
					Paul
				</label>
				<label>
					<input type="radio" name="radio" strapi-control-value="age" /> Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), sorted by either first names or age depending on whether or not the corresponding checkbox type `input` elements is selected.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use checkbox type input elements in webflow -->
		<form>
			<!-- you must use strapi-control-value for checkboxes -->
			<div strapi-sort-control="">
				<label>
					<input type="checkbox" strapi-control-value="first_name" /> Paul
				</label>
				<label>
					<input type="checkbox" strapi-control-value="age" /> Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

### strapi-control-value

The `strapi-control-value` attribute is used on elements which are children of an element with one of the `strapi-filter-control`, `strapi-sort-control` or `strapi-page-control` attributes. The allows for the use of inputs which exists as multiple elements such as in the case with `select`/`option` elements, radio `input` elements and checkbox `input` elements. See the sections for `strapi-filter-control`, `strapi-sort-control` or `strapi-page-control` for examples of how to use this attribute.

---

### strapi-state-element

The `strapi-state-element` attribute specifies an element to be hidden or shown based on the state of the parent Strapify element. Elements with this attribute must be a descendant of an element with a `strapi-collection`, `strapi-relation`, `strapi-repeatable`, `strapi-single-type-relation`, `strapi-single-type-repeatable`, `strapi-auth`, `strapi-form` or `strapi-ezforms-form` attribute.

The possible values are loading, error and success. This is useful to show an element that indicates the collection is loading, or to display error/success messages to the user. It may also be used to display success/error messages on form and auth register/login attempts.

Below is the HTML to render a collection Person (plural people), with three state elements to display a message indicating an error, success or a loading state.

```html
<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name</p>
		<p strapi-field="age">age</p>
	</div>

	<p strapi-state-element="loading">LOADING...</p>
	<p></p>
	<p strapi-state-element="success">SUCCESS</p>
	<p></p>
	<p strapi-state-element="error">ERROR</p>
	<p></p>
</div>
```

Below is the HTML to use state elements with a `strapi-auth` element.

```html
<form strapi-auth="authenticate">
	<label for="username">Username</label>
	<input
		type="text"
		placeholder="Enter Username"
		name="username"
		strapi-auth-input="identifier"
		required
	/>

	<label for="psw">Password</label>
	<input
		type="password"
		placeholder="Enter Password"
		name="psw"
		strapi-auth-input="password"
		required
	/>

	<button type="submit" strapi-auth-submit>Login</button>

	<p strapi-state-element="loading">LOADING...</p>
	<p></p>
	<p strapi-state-element="success">SUCCESS</p>
	<p></p>
	<p strapi-state-element="error">ERROR</p>
	<p></p>
</form>
```

**Allowed Elements:**

Any.

**Related Attributes:**

`[strapi-collection](Strapify%20Docs%203c7d220c5c6e4306baad33b1d2890f94.md)`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name                 | Value   | HTML                               | Description                                                                                                    |
| -------------------- | ------- | ---------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| strapi-state-element | loading | <p strapi-state-element="loading"> | The p element is displayed only when the parent collection element is loading the Strapi data.                 |
| strapi-state-element | success | <p strapi-state-element="success"> | The p element is displayed only when the parent collection element has loaded the data and finished rendering. |
| strapi-state-element | error   | <p strapi-state-element="error">   | The p element is displayed only when the parent collection element has failed to retrieve the Strapi data.     |

### strapi-delete

The `strapi-delete` attribute will mark elements to be deleted from the page before Strapify runs. This is intended as a temporary measure for debugging purposes.

Below is the HTML to render a collection Person (plural people) as well as a single type field called email in the single type collection info. The single type element will be deleted before Strapify runs.

```html
<p strapi-single-type="info.email" strapi-delete="">company email here</p>

<div strapi-collection="people">
	<div strapi-template="">
		<p strapi-field="name">name</p>
		<p strapi-field="age">age</p>
	</div>
</div>
```

**Allowed Elements:**

Any.

**Related Attributes:**

None.

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

| Name          | Value | HTML                 | Description                                         |
| ------------- | ----- | -------------------- | --------------------------------------------------- |
| strapi-delete | N/A   | <p strapi-delete=""> | The p element will be deleted before Strapify runs. |
