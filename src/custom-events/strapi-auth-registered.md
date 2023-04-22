# strapiAuthRegistered


The `strapiAuthRegistered` event is emitted when a user has successfully registered.


Below is an example of how to use the `strapiAuthRegistered` event.

```jsx
//query select an auth element to which you would like to listen for a successful registration
const formElement = document.querySelector("#register-form");

//event emitted when the user has submitted the form and the registration succeeded
formElement.addEventListener("strapiAuthRegistered", (event) => {
	//you have access the authenticated user data
	const userData = event.detail.user;

	//custom code...
});
```