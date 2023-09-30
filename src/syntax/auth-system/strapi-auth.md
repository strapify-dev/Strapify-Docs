# strapi-auth

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

`strapi-auth` is the first attribute that should be added to a login or register form when configuring the Strapify authentication system.

The basic authentication system for Strapify consists of three parts:

1. The `strapi-auth` attribute, which can be set to either "authenticate" or "register" to indicate the form's purpose.
2. The `strapi-auth-input` attribute, which can be set to the Strapi data field. For login, the keyword "identifier" is reserved for the username. For registration, the attribute can be set to the field names such as "username", "email", "password" etc.
3. The `strapi-auth-submit` attribute, which submits the form when clicked.

The Strapify auth system is intended for use on simple projects and it’s primary use is to show or hide Strapi collections depending on whether the user is logged in.

> Please Note - When working with sensitive data or on projects that require any level of complexity beyond showing/hiding collections, the Strapify auth system is not recommended.

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

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**


```html
<form strapi-auth="authenticate">
```
Marks the form element as a form that should authenticate users using the Strapify authentication system

```html
<form strapi-auth="register">
```
Marks the form element as a form that should register users using the Strapify authentication system