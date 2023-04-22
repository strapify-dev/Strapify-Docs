# strapiAuthRegisterError

The `strapiAuthRegisterError` event is emitted when a user has submitted the registration form and the registration has failed.

Below is an example of how to use the `strapiAuthRegisterError` event.

```jsx
//query select an auth element to which you would like to listen for a failed registration
const formElement = document.querySelector("#register-form");

//event emitted when the user has submitted the form and the registration failed
formElement.addEventListener("strapiAuthRegisterError", (event) => {
	//you have access to the error message and the full javascript error
	const error = event.detail.error;
	const errorMessage = event.detail.errorMessage;

	//custom code...
});
```