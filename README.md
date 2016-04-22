# WCAG 2.0
Web Content Accessibility Guidelines (WCAG) 2.0 covers a wide range of recommendations for making Web content more accessible. Great easy to read WCAG 2.0 Techniques.

## Form Controls

The objective of this technique is to use the `label` element to explicitly associate a form control with a label. A `label` is attached to a specific form control through the use of the `for` attribute. The value of the `for` attribute must be the same as the value of the `id` attribute of the form control.

The `id` attribute may have the same value as the `name` attribute, but both must be provided, and the `id` must be unique in the Web page.  

Elements that use explicitly associated labels are:

	input type="text"
	input type="checkbox"
	input type="radio"
	input type="file"
	input type="password"
	textarea
	select


### Examples

Example 1: A text input field

	<label for="firstname">First name:</label> 
	<input type="text" name="firstname" id="firstname" />

Example 2: A checkbox

	<input type="checkbox" id="markuplang" name="computerskills" checked="checked">
	<label for="markuplang">HTML</label>

Example 3: A group of radio buttons

	<h1>Donut Selection</h1>
	
	<p>Choose the type of donut(s) you would like then select 
	   the "purchase donuts" button.</p>
	
	<form action="http://example.com/donut" method="post">
	<p>
	  <input type="radio" name="flavor" id="choc" value="chocolate" />
	    <label for="choc">Chocolate</label><br/>
	  <input type="radio" name="flavor" id="cream" value="cream"/>
	    <label for="cream">Cream Filled</label><br/>
	  <input type="radio" name="flavor" id="honey" value="honey"/>
	    <label for="honey">Honey Glazed</label><br/>
	  <input type="submit" value="Purchase Donuts"/>
	</p>
	</form>

### Tests

For all input elements of type `text`, `file`, `textareas` or `password`, and for all `select` elements in the Web page:

1. Check that there is a `label` element that identifies the purpose of the control before the `input`, `textarea`, or `select` element
2. Check that the `for` attribute of the `label` element matches the `id` of the `input`, `textarea`, or `select` element
3. Check that the `label` element is visible.

For all input elements of type `checkbox` or `radio` in the Web page:

1. Check that there is a `label` element that identifies the purpose of the control after the `input` element
2. Check that the `for` attribute of the label element matches the `id` of the `input` element
3. Check that the `label` element is visible.

##Groups of Form Controls
The objective of this technique is to provide a semantic grouping for related form controls. This allows users to understand the relationship of the controls and interact with the form more quickly and effectively.

Form controls can be grouped by enclosing them within the `fieldset` element. All controls within a given `fieldset` are then related. The first element inside the `fieldset` must be a `legend` element, which provides a label or description for the group. Authors should avoid nesting `fieldsets` unnecessarily, as this can lead to confusion.

### Examples

Example 1: A multiple choice test

	<fieldset>
	  <legend>The play <cite>Hamlet</cite> was written by:</legend>
	  <input type="radio" id="shakesp" name="hamlet" checked="checked" value="a">
	  <label for="shakesp">William Shakespeare</label><br />
	  <input type="radio" id="kipling" name="hamlet" value="b">
	  <label for="kipling">Rudyard Kipling</label><br />
	  <input type="radio" id="gbshaw" name="hamlet" value="c">
	  <label for="gbshaw">George Bernard Shaw</label><br />
	  <input type="radio" id="hem" name="hamlet" value="d">
	  <label for="hem">Ernest Hemingway</label><br />
	  <input type="radio" id="dickens" name="hamlet" value="e">
	  <label for="dickens">Charles Dickens</label>
	</fieldset>  
