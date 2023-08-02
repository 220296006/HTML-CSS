# Working with Forms and Interactive Elements

## Form Fundamentals

Form fields have been an essential part of the web for a long time. They are used for various tasks like logging into websites, making purchases, conducting searches, and adding content. 

It is important to use semantic form elements in HTML instead of divs and spans because it allows us to leverage the built-in power of the browser. This way, we avoid wasting time and effort trying to recreate functionalities that already exist in the browser. Moreover, by using HTML form elements, we ensure that forms will be compatible with all devices and input/output hardware, even those we may not be familiar with. 

To create a form, we start with the form element, which informs the browser about the presence of a form using opening and closing tags. In the newsletter signup form, there will be two fields: name and email. These field names can be turned into labels using the label element. 

Use the input element to provide places for users to input their name and email. Unlike other elements, the input element does not have a closing tag due to its older structure. It acts as a marker for the browser to bring in functionality and place it there. This is where the form's magic happens. 

Now, a button is needed for users to submit the form. Use the button element for this. The text on the button can be customized to whatever is required. Although the form looks good visually, it currently lacks functionality. To make it work, we need to connect it to a backend. We can add an action and method attribute to make a demo work, although using the "get" method is not secure and is not recommended for real websites.

## More Form Functions

###  The Form label 

The HTML form element is used to create an HTML form for user input:

<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, you will submit your data.</p>

### The Input label  

The HTML input element is the most used form element.

An input element can be displayed in many ways, depending on the type attribute.

Type	Description
<input type="text">	Displays a single-line text input field
<input type="radio">	Displays a radio button (for selecting one of many choices)
<input type="checkbox">	Displays a checkbox (for selecting zero or more of many choices)
<input type="submit">	Displays a submit button (for submitting the form)
<input type="button">	Displays a clickable button

### Text Fields

The <input type="text"> defines a single-line input field for text input.


### The Label element

The <label> tag defines a label for many form elements.

The <label> element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focuses on the input element.

The <label> element also helps users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the <label> element, it toggles the radio button/checkbox.

The for attribute of the <label> tag should be equal to the id attribute of the <input> element to bind them together.


### Radio Buttons

The <input type="radio"> defines a radio button.

Radio buttons let a user select ONE of a limited number of choices.

<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>

### Checkboxes

The <input type="checkbox"> defines a checkbox.

Checkboxes let a user select ZERO or MORE options of a limited number of choices.

<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label>
</form>


### The Submit Button

The <input type="submit"> defines a button for submitting the form data to a form-handler.

The form-handler is typically a file on the server with a script for processing input data.

The form-handler is specified in the form's action attribute.

<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>

