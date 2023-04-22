# strapi-state-element

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

**Allows Multiple Arguments:** 🚫 **NO**

### Examples

```html
<p strapi-state-element="loading">LOADING...</p>
```
The p element is displayed only when the parent collection element is loading the Strapi data.

```html
<p strapi-state-element="success">SUCCESS</p>
```
The p element is displayed only when the parent collection element has loaded the data and finished rendering.

```html
<p strapi-state-element="error">ERROR</p>
```
The p element is displayed only when the parent collection element has failed to retrieve the Strapi data.