# strapi-single-type-background-image

The `strapi-single-type-background-image` works the same as the [strapi-background-image](strapi-background-image.md) attribute, but it is used on a single type element instead of a collection element.

## Example

```html
<div strapi-single-type-background-image="homepage.background">
    <h1 strapi-single-type="homepage.title"></h1>
    <p strapi-single-type="homepage.text">Some text</p>
</div>
```
This example sets the background image of the div to the value in the single type "homepage" with the field "background".