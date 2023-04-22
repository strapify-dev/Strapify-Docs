# strapi-page-control

The `strapi-page-control` attribute is used on input elements, such as buttons, radio buttons and selects. This attribute accepts either a number, which will directly set the page of the collection element, or a sign prefixed number which will increment/decrement that page by the number that follows.

Below is the HTML to paginate and render render a collection Person (people), with a button to go to the first page, next page and previous page.

```html
<div strapi-collection="people" strapi-page="1" strapi-page-size="4">
	<a strapi-page-control="1">First Page</a>
	<a strapi-page-control="+1">Next Page</a>
	<a strapi-page-control="-1">Prev Page</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to paginate and render render a collection Person (people), with a select option for the first four pages.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not optional here -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- using value -->
			<select strapi-page-control="">
				<option value="1">1</option>
				<option value="2">2</option>
				<option value="3">3</option>
				<option value="4">4</option>
			</select>

			<!-- using strapi-control-value -->
			<select strapi-page-control="">
				<option strapi-control-value="1">1</option>
				<option strapi-control-value="2">2</option>
				<option strapi-control-value="3">3</option>
				<option strapi-control-value="4">4</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to paginate and render render a collection Person (people), with a radio button for the first two pages.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is optional here -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- using value -->
			<div strapi-page-control="">
				<label> <input type="radio" name="radio" value="1" /> Paul </label>
				<label> <input type="radio" name="radio" value="2" /> Richard </label>
			</div>

			<!-- using strapi-control-value -->
			<div strapi-page-control="">
				<label>
					<input type="radio" name="radio" strapi-control-value="1" /> Paul
				</label>
				<label>
					<input type="radio" name="radio" strapi-control-value="2" /> Richard
				</label>
			</div>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

**Allowed Elements:**

`a` `button` `select` `input type="radio"` `input type="checkbox"`

**Allows Multiple Arguments:** 🚫 **NO**