# strapi-filter-control

The `strapi-filter-control` attribute is used on input elements, such as buttons, radio buttons, selects and check boxes. When the input element triggers an event, the value of the attribute will set the value of `strapi-filter` on the parent collection element, and the collection will be rerendered with the new filter. The value of this attribute will be the new value of `strapi-filter` on the parent collection when the input event is triggered.

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two possible `a` elements is clicked.

```html
<div strapi-collection="people">
	<a strapi-filter-control="[first_name][$eq]=Paul">Filter by Paul</a>
	<a strapi-filter-control="[first_name][$eq]=Richard">Filter by Richard</a>

	<div>
		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two options in a `select` is chosen.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use select elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for option elements -->

			<!-- this way will work with webflow (using value) -->
			<select strapi-filter-control="">
				<option value="[first_name][$eq]=Paul">Paul</option>
				<option value="[first_name][$eq]=Richard">Richard</option>
			</select>

			<!-- this is the second way (using strapi-control-value) -->
			<select strapi-filter-control="">
				<option strapi-control-value="[first_name][$eq]=Paul">Paul</option>
				<option strapi-control-value="[first_name][$eq]=Richard">
					Richard
				</option>
			</select>
		</form>

		<div strapi-template="">
			<p strapi-field="first_name">first name here</p>
			<p strapi-field="age">age here</p>
		</div>
	</div>
</div>
```

Below is the HTML to filter a collection Person (people), filtered by the first names Paul or Richard when one of two `radio` buttons is clicked.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use radio type input elements in webflow -->
		<form>
			<!-- there are two valid ways to specify the control value for radio elements -->

			<!-- this way will work with webflow (using value) -->
			<div strapi-filter-control="">
				<label>
					<input type="radio" name="radio" value="[first_name][$eq]=Paul" />
					Paul
				</label>
				<label>
					<input type="radio" name="radio" value="[first_name][$eq]=Richard" />
					Richard
				</label>
			</div>

			<!-- this is the second way (using strapi-control-value) -->
			<div strapi-filter-control="">
				<label>
					<input
						type="radio"
						name="radio"
						strapi-control-value="[first_name][$eq]=Paul"
					/>
					Paul
				</label>
				<label>
					<input
						type="radio"
						name="radio"
						strapi-control-value="[first_name][$eq]=Richard"
					/>
					Richard
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

Below is the HTML to filter a collection Person (people), filtered by the first names Paul and/or Richard depending on whether or not the corresponding checkbox type `input` elements is selected. Since both checkboxes can be selected at once, the logical `[$or]` Strapi operator is used.

```html
<div strapi-collection="people">
	<div>
		<!-- a form element is not needed here but is necessary to use checkbox type input elements in webflow -->
		<form>
			<!-- you must use strapi-control-value for checkboxes -->
			<div strapi-filter-control="">
				<label>
					<input
						type="checkbox"
						strapi-control-value="[$or][0][first_name][$eq]=Paul"
					/>
					Paul
				</label>
				<label>
					<input
						type="checkbox"
						strapi-control-value="[$or][1][first_name][$eq]=Richard"
					/>
					Richard
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