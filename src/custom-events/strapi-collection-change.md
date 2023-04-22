# strapiCollectionChange

This event is emitted when a collection, relation or repeatable element is rerendered or rendered for the first time.

Below is an example of how to use the `strapiCollectionChange` event. This event is use on collection, relation and repeatable elements.

```jsx
//query select a collection element to which you would like to listen for changes
const peopleCollectionElement = document.querySelector("#people-collection");

//event emitted when the collection is rerendered or rendered for the first time
peopleCollectionElement.addEventListener(
	"strapifyCollectionChange",
	(event) => {
		//you have access to the collection element that changed and the collection data that was fetched.
		const collectionElement = event.target;
		const strapiCollectionData = event.detail.collectionData;

		//custom code...
	}
);
```