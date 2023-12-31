# strapi-logout

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

When set on a `<button>` element, the `strapi-logout` attribute will log out the user when the button is clicked. It can be used together with `strapi-logout-redirect` to destroy the token and redirect the user to another page.

### Example

```html
<button strapi-logout>Logout</button>
```
Log out the user when the button is clicked.

```html
<button strapi-logout strapi-logout-redirect="/home">Logout</button>
```
Log out the user and redirect them to the `/home` page.