## 5.4. Creating Forms
<br/>

1. Creating Forms and Binding Data


First create a state variable to hold the data of the form (i.e. formData)

Next create a form widget, and place required widgets(i.e. text boxes) inside it.

Select form widget and bind the state variable to it (i.e. formData) for the property Form Binding

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0092.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0093.png"/>


Next, select individual widgets such as text boxes and bind state variables for the Value Binding property.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0094.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0095.png"/>


2. Adding Validations for Individual Widgets within the Form

To add validations to individual form widgets, you can open the Form Validation tool window and add the required validations.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0096.png"/>


3. Validating the Form


For example, to validate the form when the user clicks on a button, you can use the block “Validate Form” which can be found under the toolbar category “Frontend App”. For that block you can select the form element that is required to be validated. 

To ensure that the form is being validated, you can use an If block.

To submit data to a thirh party API you can use the blocks that are under the toolbar category “Integration”

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0097.png"/>
