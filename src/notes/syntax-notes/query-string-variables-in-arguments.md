# Query String Variables in Arguments

Query string arguments are arguments that contain a placeholder for a value contained in the current page’s query string, notated by a **_qs._** prefix, example: **_qs.varName_**. When strapify finds an occurrence of a query string argument, it will be replaced entirely by the value of the query string parameter with the specified name. For example **_qs.varName_** would be replaced by **_varValue_** if the query string for the page was **_?varName=varValue_**. A few more examples are shown in the table below. Query string variables may be used in any Strapify attribute value.

| Website Query String      | Given Attribute Value      | Strapify Uses             |
| ------------------------- | -------------------------- | ------------------------- |
| ?message=hello            | qs.message                 | hello                     |
| ?nameComponentField=first | name.qs.nameComponentField | name.first                |
| ?title=movie review       | [title][$eq]=qs.title      | [title][$eq]=movie review |

There may be situations where you wish to render a single entry in a Strapi collection on a dedicated page. For example, if you had a collection Blogs, you may wish to have a separate page for each Blog belonging to Blogs. Strapify allows this situations through query string arguments, which you would write in the URL when you link to the page for the blog. Consider the following Strapi collection.

> collection name: Blog
>
> - field name: title
> - field name: rich_text

Now let’s say you want to have a page for a blog in the collection with title “fun day at the beach.” and another page for a blog with title “bad day at home.”. To do this create a page called www.yourwebsite.com/blog and on that page, create a collection element as you would normally. Now to link to that URL in a way that will allow you display only the “fun day at the beach blog”, you would use the URL www.yourwebsite.com/blog?title=fun day at the beach. On your blog page, the query string parameter will be available in your strapi arguments, which you can use to filter out a single blog to display. You would use the following attributes on the collection element your created:

`strapi-collection="blogs"` , `strapi-filter="[title][$eq]=qs.title"`

If you wanted to instead link to the blog with title “bad day at home”, you would use the URL www.yourwebsite.com/blog?title=bad day at home.