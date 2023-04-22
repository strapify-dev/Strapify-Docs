# strapi-success-redirect

The `strapi-success-redirect` attribute redirects a user to a different URL when a `strapi-ezforms-form` or `strapi-auth` form is successfully submitted. It should be added on the `<form>` component itself.

### Example

```html
<form strapi-ezforms-form strapi-success-redirect="/success">
```

Redirects the user to the success page when the form submission is successful