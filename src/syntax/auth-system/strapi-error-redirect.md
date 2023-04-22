# strapi-error-redirect

The `strapi-error-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form fails to submit. It should be added on the `<form>` component itself.

### Example

```html
<form strapi-ezforms-form strapi-error-redirect="/error">
```

Redirects the user to the error page when the form submission is unsuccessful