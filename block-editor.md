### Block Editor Guidelines
<br/>
Block editor enables you to specify your logic for endpoints and admin workflows. 
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_1.png"/><br/><br/>

#### Toolbar Categories and Toolbar Category Types
<br/>
Toolbar Categories are defined by a name (i.e. Triggers, Flow, String, etc...) that enables the developers to easily search and locate a block on the toolbar.
<br/><br/>
Toolbar Category Types are defined by a color code that also further subdivide a block category which makes it easier for the developer to identify the category of a block, especially when one block is used on the editor.

<br/><br/>

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_2.png"/>&nbsp;&nbsp;&nbsp;Triggers (i.e. Adding business logic, authorization logic)
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_3.png"/>&nbsp;&nbsp;&nbsp;Control Flow (i.e. if, for,  functions etc...)
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_4.png"/>&nbsp;&nbsp;&nbsp;Data Types and variables (i.e. creating string, creating numbers, modifying strings, arithmetic, etc..) 
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_5.png"/>&nbsp;&nbsp;&nbsp;Other (i.e. Connecting to MySQL, calling 3rd party REST APIs, logging, etc...)
<br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_6.png"/><br/><br/>

#### Block types
<br/>
There are three blocks types which can easily be identified by their shapes. Block types also provide a particular type of behavior.
<br/><br/>

##### Statement Blocks 
<br/>
A statement block performs some activity and returns a value, Statement blocks can be connected vertically with other statement blocks. Statement block should only placed inside a trigger body or inside a control flow body.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_7.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_8.png"/>
<br/><br/><br/>

##### Function Blocks
<br/>
When a statement block outputs a value, the output can be sent as an input to a function block. Each function block also performs an activity and return an output. Function blocks can be chained horizontally.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_9.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_10.png"/>
<br/><br/><br/>


##### Control Flow Blocks

All the other remaining block types belong to this category such as triggers, if-else blocks, functions, etc...
<br/><br/><br/>


#### Variables, References, and Expressions
<br/>
On the toolbar some blocks enable the developer to manage various variables and references for variables. Such blocks have a text input on them which a placeholder.
Blocks that create or modify variables have 'set_variable' placeholder.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_11.png"/>
<br/><br/><br/>
Blocks that require a value (the value can also be a reference to another variable). Such blocks have a placeholder '{{reference}}'. you can place the variable name inside the curly brackets.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_12.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_13.png"/>
<br/><br/><br/>
Expressions perform an evaluation such as an arithmetic, or a logic for an if condition.
<br/><br/><br/>

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_14.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_15.png"/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_16.png"/>
<br/><br/>

#### Triggers
<br/>
Triggers are used to respond to various events that occur within an endpoint. For example "When the Request Arrives" trigger can be used to add logic that should occur prior to executing the API endpoint logic (i.e. you can perform a JWT token validation in that trigger). Also the "Request Handling Logic" trigger is used to define the logic of the API endpoint.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_17.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_18.png"/>
<br/><br/><br/>

#### Setting the response of an endpoint
<br/>
Set response blocks are used to define the response of the API endpoint. There are two variations of "Set Response" blocks which one is a statement block, and the other is a function block. 
As you see on the first picture, the "Set Response" function block is used to set the string value returned from the previous block.
Similarly, The statement "Set Response" block can be used to return a reference to a variable or a value as the endpoint response.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_19.png"/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_20.png"/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_21.png"/><br/>
<br/><br/><br/>

#### Template Strings
<br/>
On the properties panel, when you assign a value for a particular property, you can assign the value as a template string. Template strings start with $ sign and include variables within curly brackets.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_22.png"/><br/><br/><br/>

#### Flow control blocks
<br/>
Control flow blocks are used to manage the flow of the API endpoint.<br/>
The following example shows an if condition.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_23.png"/>
<br/><br/><br/>
The following example shows how to define a function and how to call a function within a trigger.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/3_24.png"/>
<br/><br/><br/>