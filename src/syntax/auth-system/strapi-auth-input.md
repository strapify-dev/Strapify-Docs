# strapi-auth-input

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

> When working with sensitive data or on projects that require any level of complexity beyond showing/hiding collections, the Strapify auth system is not recommended.

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

**Allows Multiple Arguments:** ✅ YES

### Examples

```html
<input type="text" name="username" strapi-auth-input="identifier" />
```
Marks the username input as the identifier used for authentication (login).

```html
<input type="text" name="username" strapi-auth-input="username">
```
Another username input, however this would be used for registration to set the new user’s username

```html
<input type="text" name="username" strapi-auth-input="username | email">
```
Another username input, however this would be used for registration to set the new user’s username and email to the value entered in the username input.