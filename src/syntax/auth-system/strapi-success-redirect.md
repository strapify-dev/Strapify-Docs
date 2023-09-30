# strapi-success-redirect

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

The `strapi-success-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form is successfully submitted. It should be added on the `<form>` component itself.

### Example

```html
<form strapi-ezforms-form strapi-success-redirect="/success">
```

Redirects the user to the success page when the form submission is successful