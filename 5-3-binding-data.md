## 5.3. Binding Data With MVVM Pattern
<br/>

1. MVVM Pattern Overview

NoCodeXpress uses the MVVM (Mode-View-ViewModel) Design Pattern to represent data to the UI. The MVVM pattern is used in Frontend frameworks such as Angular or Vue which are written in JavaScript. Therefore NoCodeXpress enables the developer to use the MVVM pattern with no-coding.

MVVM Pattern is proven to be effective to represent, submit, and manipulate data effectively for the UIs. For example when you retrieve the data from a REST API you can easily represent the data on the UI using the pattern, or when you create a form the pattern can be used for form submission too.

Explained simply, what it does is when a state variable changes in the states the change is automatically reflected on the UI without any extra work, and also when a state variable is bound to a widget (i.e. a textbox) when the user changes the value of the widget (i.e. textbox) it will automatically change the state variable .




2. Creating State Variables and Binding State Variables to Widgets

To create a state variable you need to open the tool window “State / Properties” On the tool window you can define the names for the state variables. If you click on the pen icon, you can configure more settings for the state variable such as its data type, its default value. 

You can also trigger an event and create your logic with blocks when the state variable changes by creating an event under the “On Change” value.
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0082.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0083.png"/>



To bind the state variable to the widget, select the widget and open any tool window and choose a property of the widget that you need to bind the state variable to. For example you need to open “Selected Item Properties” tool window if you need to bind the state varlable to the “Caption” property of a label.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0084.png"/>


Next click on the bind icon which will open the popup to bind the state variable. and select “current” as the state. Then you can select the state variable you have created from the “Field” dropdown.

If you have binded an object, and you need to bind a field of that object (i.e. firstName property of an object) you can specify the field name (i.e. firstName) in the text box sub field.





3. Modifying State Variables from Blocks

Let’s assume that you need to change the state variable from the previous example firstName when the user clicks on a button. When the state variable changes all the widgets which have that state variable bound to those will change their properties.

First drag and drop a button on to the UI, and create a click event for that.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0085.png"/>


Under the click event, create a string variable with the value “Hello World”

And use the block “And Set UI State Variable” which accepts string input and update the state variable.

When the user clicks on the button, it will update the state variable, and the changes will be reflected on the UI

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0086.png"/>


4. Creating Repeaters (for Visualizing Arrays on the UI)

When you have an array of data you need to represent the UI, you can bind the array as a “Repeater” to a widget. When you run the application all the array items will be created on the UI with a corresponding widget you have binded the state variable to. For example, if you have a number array of 3 items and you have binded the array to a label. When you run the UI 3 labels will be created to represent the array. As you keep of adding, removing items from the array, the UI gets updated.

After you create a state variable with the data type “array”, to create a repeater for a widget open the tool window “Selected Item Extra Configuration”. Under the “Repeat” property you can apply the binding for the array state variable.

Let’s assume the array consists of a list of customers, which each element has its unique key/identifier as “id”. In this case you can specify “id” as the unique key parameter.

It's also mandatory to specify a repeat variable. The repeat variable also becomes a read-only state variable that can be binded to a widget. The repeat variable also represents a single variable which can be binded to a widget

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0087.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0088.png"/>


It's also mandatory to specify a repeat variable. The repeat variable represent an individual element of the array. The repeat variable can be binded to the same widget or its child widgets. By selecting the scope as “repeat” like in the following picture, you can select the repeat variable. If there’s a sub field for the repeat variable you can enter the sub field as well.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0089.png"/>


5. Executing an event when a state variable changes


To execute an event when the state variable changes, you can add a new event handler under the “On change” parameter when you create the state variable. You can specify the logic with blocks for the event.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0090.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0091.png"/>
