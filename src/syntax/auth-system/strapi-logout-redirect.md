# strapi-logout-redirect

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

> When working with sensitive data or on projects that require any level of complexity beyond showing/hiding collections, the Strapify auth system is not recommended.

The `strapi-logout-redirect` attribute can be used on a `strapi-logout` element to redirect a user to a different URL when the element is clicked. This is useful for logging out a user and redirecting them to a different page.

### Example

```html
<button strapi-logout strapi-logout-redirect="/home">Logout</button>
```
Log out the user and redirect them to the `/home` page.