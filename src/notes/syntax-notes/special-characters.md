# Special Characters

- Note that some special characters including ampersands (&) should be encoded manually in your attribute values. For example if you’re trying to filter by a Category field equal to “Rice & Beans”, the value would be `strapi-filter=[Category][$eq]=Rice %26 Beans` rather than `strapi-filter=[Category][$eq]=Rice & Beans`