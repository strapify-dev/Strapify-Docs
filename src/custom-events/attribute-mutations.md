# Attribute Mutations

Some Strapify elements will automatically respond to changes made to their HTML attributes. When these mutations occur the collection will rerender using the new the attribute values. This allows custom scripts to change the filter, sort and page of collection elements, for example.

Elements that support attribute mutations:

- collection elements
- field elements
- relation elements
- repeatable elements
- single type field elements

Below is an example of how to mutate a the strapi-filter value on a Strapify collection.

```js
// select a collection element so we can change its strapi-filter-control value
const collectionElement = document.querySelector("#people-collection");

// Set the new attribute value and Strapify will rerender the collection accordingly
collectionElement.setAttribute("strapi-filter", "[name][$eq]=Austin");
```