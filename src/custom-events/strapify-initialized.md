# strapifyInitialized

The `strapifyInitialized` event is emitted when strapify finishes rendering for the first time. All Strapi data will have been rendered to the DOM before this event occurs.

Below is an example of how to use the `strapifyInitialized` event.

```jsx
//emitted when strapify finishes rendering for the first time
//all Strapi data will have been rendered to the DOM before this event occurs
document.addEventListener("strapifyInitialized", (event) => {
	//you have access the authentication state and the user data if authenticated
	const userAuthenticated = event.detail.userAuthenticated;
	const userData = event.detail.user;

	//custom code that interacts with strapify...
	//or any custom code that requires that strapify has already rendered...
	//or any custom code that requires access to authenticated user information...
});
```