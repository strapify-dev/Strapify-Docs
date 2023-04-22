# strapiUserAuthenticated

This event is emitted when Strapify runs and validates existing user data from local storage.  

Below is an example of how to use the `strapiUserAuthenticated` event.

```jsx
//event emitted when Strapify runs and validates existing user data from local storage
document.addEventListener("strapiUserAuthenticated", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```