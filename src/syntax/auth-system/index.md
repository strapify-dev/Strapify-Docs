# Auth System (Alpha)

Strapify provides a basic authentication system that can be used to authenticate users and register new users.  It is intended for use on simple projects and it’s primary use is to show or hide Strapi collections depending on whether the user is logged in.

> Please Note - The auth system stores the user's JWT in local storage.  This is not secure and should not be used for sensitive data.  Soon, the auth system will be updated to use secure cookies instead of local storage, but for now, please do not use the auth system for sensitive data.

The basic authentication system for Strapify consists of three parts:

1. The [strapi-auth](strapi-auth.md) attribute, which can be set to either "authenticate" or "register" to indicate the form's purpose.
2. The [strapi-auth-input](strapi-auth-input.md) attribute, which can be set to the Strapi data field. For login, the keyword "identifier" is reserved for the username. For registration, the attribute can be set to the field names such as "username", "email", "password" etc.
3. The [strapi-auth-submit](strapi-auth-submit.md) attribute, which submits the form when clicked.