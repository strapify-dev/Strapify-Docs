# strapi-sort-control

The `strapi-sort-control` attribute is used on input elements, such as buttons, radio buttons, selects and check boxes. When the input element triggers an event, the value of the attribute will set the value of `strapi-sort` on the parent collection element, and the collection will be rerendered with the new sort. The value of this attribute will be the new value of `strapi-sort` on the parent collection when the input event is triggered.

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of the `a` elements is clicked.

```html
<div strapi-collection="people">
	<a strapi-sort-control="first_name">Filter by name</a>
	<a strapi-sort-control="age">Filter by age</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of two options in a `select` is chosen.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use select elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- this way will work with webflow (using value) -->
			<select strapi-sort-control="">
				<option value="first_name">Paul</option>
				<option value="age">Richard</option>
			</select>

			<!-- this is the second way (using strapi-control-value) -->
			<select strapi-sort-control="">
				<option strapi-control-value="first_name">Paul</option>
				<option strapi-control-value="age">Richard</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), sorted by either first names or age when one of two `radio` buttons is clicked.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use radio type input elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- this way will work with webflow (using value) -->
			<div strapi-sort-control="">
				<label>
					<input type="radio" name="radio" value="first_name" /> Paul
				</label>
				<label> <input type="radio" name="radio" value="age" /> Richard </label>
			</div>

			<!-- this is the second way (using strapi-control-value) -->
			<div strapi-sort-control="">
				<label>
					<input type="radio" name="radio" strapi-control-value="first_name" />
					Paul
				</label>
				<label>
					<input type="radio" name="radio" strapi-control-value="age" /> Richard
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

Below is the HTML to filter a collection Person (people), sorted by either first names or age depending on whether or not the corresponding checkbox type `input` elements is selected.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use checkbox type input elements in webflow -->
		<form>
			<!-- you must use strapi-control-value for checkboxes -->
			<div strapi-sort-control="">
				<label>
					<input type="checkbox" strapi-control-value="first_name" /> Paul
				</label>
				<label>
					<input type="checkbox" strapi-control-value="age" /> Richard
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