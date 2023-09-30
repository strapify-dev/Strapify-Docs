# strapi-error-redirect

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

> When working with sensitive data or on projects that require any level of complexity beyond showing/hiding collections, the Strapify auth system is not recommended.

The `strapi-error-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form fails to submit. It should be added on the `<form>` component itself.

### Example

```html
<form strapi-ezforms-form strapi-error-redirect="/error">
```

Redirects the user to the error page when the form submission is unsuccessful