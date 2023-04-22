# strapiUserAuthenticationError

This event is emitted when Strapify runs and failed to validate existing user data.

Below is an example of how to use the `strapiUserAuthenticationError` event. When user data is found but could not be validated this event will fire. Currently, the invalid user data is just deleted and the page is reloaded immediately, so this event will never be used at the moment. An option to prevent an automatic page reload may be added in the future.

```jsx
//event emitted when Strapify runs and failed to validate existing user data
document.addEventListener("strapiUserAuthenticationError", (event) => {
	//custom code...
});
```