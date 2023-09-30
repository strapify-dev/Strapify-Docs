# strapi-auth-submit

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

The `strapi-auth-submit`attribute should be used in `strapi-auth` forms to indicate the submit button. When clicked, it triggers the authentication process (either registration or login). The attribute is typically added to a `<button>` element of type "submit".

If `strapi-auth` is set to `register`, the form will attempt to create a new user from the credentials provided in the form inputs using `strapi-auth-input`.

If `strapi-auth` is set to `authenticate`, it will attempt to authenticate the user based on the credentials provided in the login form, and the user’s JWT token will be stored in localStorage.

---

**Allowed Elements:**

`button`

**Allows Multiple Arguments:** 🚫 **NO**

**Examples:**

See code example in [strapi-auth](strapi-auth.md)