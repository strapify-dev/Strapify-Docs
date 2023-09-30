# Getting Started

To start using Strapify, you'll need a running Strapi application.  You can create a new one using the [Quick Start Guide](https://docs.strapi.io/dev-docs/quick-start) or use an existing one.  Strapify is compatible with Strapi v4 only.

First, you'll need to include the Strapify script in your HTML document.  You can do this by downloading the script and hosting it yourself, or by using the CDN version.

## Downloading the Script

⬇️ [Download](https://strapify.s3.amazonaws.com/strapify-v0.0.7.js)

## Using the CDN

Paste the following code in the ```<head>``` of your HTML document.

```html
<script
    src="https://strapify.s3.amazonaws.com/strapify-v0.0.7.js"
    data-strapi-api-url="ENTER YOUR STRAPI URL HERE"
    type="text/javascript"
></script>
```

## Testing the Script

Once you've included the script, you can test it by opening the console in your browser. You should see a message that says "Strapify running" and "Strapify finished".

## Connect to your first collection

To connect to your first collection, you'll need to create a new HTML element with the ```strapi-collection``` attribute.  The value of this attribute should be the name of the collection you want to connect to.  For example, if you have a collection called "articles", you would use the following code:

```html
<div strapi-collection="articles"></div>
```

## Creating your template

To display your collection, you'll need to create another HTML element inside your collection with the ```strapi-template``` attribute.  Your template element should contain the HTML you want to display for each item in your collection.  If you've connected to your collection properly, the template should be repeated for each item in the collection.

```html
<div strapi-collection="articles">
    <div strapi-template>
        some html to display for each article
    </div>
</div>
```

## Using fields in your template

To display the data from your collection, you can use the ```strapi-field``` attribute.  The value of this attribute should be the name of the field you want to display.  For example, if you have a field called "title", you would use the following code:

```html
<div strapi-collection="articles">
    <div strapi-template>
        <h1 strapi-field="title"></h1>
    </div>
</div>
```

Fields can be linked to many types of HTML elements.  For example, you can use the ```src``` attribute to display an image:

```html
<div strapi-collection="articles">
    <div strapi-template>
        <h1 strapi-field="title"></h1>
        <img strapi-field="featureImage" />
    </div>
</div>
```

A full list of supported field types can be found [here](syntax/field-elements/strapi-field.md).