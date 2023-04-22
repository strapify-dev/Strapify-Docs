# strapi-ezforms-form

The `strapi-ezforms-form` attributes is used on form elements to identify the form as one which will submit form data to the EZForms plugin endpoints in Strapi.

The [strapi EZForms plugin](https://market.strapi.io/plugins/strapi-plugin-ezforms) will have to be installed and configured. Once installed, the plugin will create two collections: "Form Sumbissions" and "Notification Recipients". The "Form Submissions" collection will be used to store form submissions, and the "Notification Recipients" collection will be used to store email addresses that will receive notifications when a form is submitted.  An email provider may also be configured if you’d like to receive email notifications on form submissions.

When submitted, it emits two custom events: `strapiEZFormsSubmitted` and `strapiEZFormsError`. These events can be used to trigger UI changes or other custom logic on form submission.

There are two other simple ways to trigger UI changes on form submission.

1. You can set `strapi-state-element` on an element to show/hide elements depending on the state of the form submission. The two key values would be `strapi-state-element="success"`, to be set on the element you’d like to show when the user successfully submits the form, and `strapi-state-element="error"`, to be set on the element you’d like to show when the form submission fails.
2. You can use `strapi-success-redirect` or `strapi-error-redirect` to redirect to a different URL when a form submission succeeds or fails.

Below is the HTML to configure a form with `strapi-ezforms-form`

```html
<form strapi-ezforms-form>
	<label for="username">Email</label>
	<input type="email" placeholder="Enter Email" name="email" required />

	<label for="message">Your Message</label>
	<input type="password" placeholder="Enter Password" name="psw" required />

	<button type="submit" strapi-ezforms-submit>Submit</button>
</form>
```

Strapify automatically parses all of the form’s input fields.  The form’s input fields will be sent to the Strapi EZForms plugin endpoint as a JSON object.  The JSON object will be stored in the "Form Submissions" collection in Strapi.  The keys of the JSON object will be the names of the input fields, and the values will be the values of the input fields.

---

**Allowed Elements:**

`form`

**Allows Multiple Arguments:** 🚫 **NO**

### Example

See code example above