# Filtering, Sorting, and Pagination

Strapify provides a number of attributes that can be used to filter, sort, and paginate your collections. These attributes are:

- [strapi-filter](strapi-filter.md) - Filter the collection by a given field.
- [strapi-sort](strapi-sort.md) - Sort the collection by a given field.
- [strapi-page](strapi-page.md) and [strapi-page-size](strapi-page-size.md) - Paginate the collection with a given number of entries per page.

These attributes can be used in conjunction with each other to create complex filtering, sorting, and pagination schemes.  For example, you can use `strapi-filter` to filter a collection by a given field, then use `strapi-sort` to sort the filtered collection by a different field, and finally use `strapi-pagination` to paginate the sorted collection.

Additionally, there are a number of attributes that can be used to control the behavior of the filtering, sorting, and pagination attributes. These attributes are:

- [strapi-filter-control](strapi-filter-control.md) - Control the behavior of the `strapi-filter` attribute.
- [strapi-sort-control](strapi-sort-control.md) - Control the behavior of the `strapi-sort` attribute.
- [strapi-page-control](strapi-page-control.md) - Control the behavior of the paginated collection.

Note: These attributes can be used even if the filtering, sorting, and pagination attributes are not used.  For example, you can use `strapi-filter-control` to control the behavior of the `strapi-filter` attribute even if you are not using the `strapi-filter` attribute.


