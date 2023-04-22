# strapiAuthLoggedIn

This event is emitted when the user has submitted the login form and the log in succeeded.

Below is an example of how to use the `strapiAuthLoggedIn` event.

```jsx
//query select an auth element to which you would like to listen for a successful log in.
const formElement = document.querySelector("#login-form");

//event emitted when the user has submitted the login form and the log in succeeded
formElement.addEventListener("strapiAuthLoggedIn", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```