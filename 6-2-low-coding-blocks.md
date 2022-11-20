## 6.2. Creating Blocks with Low-Coding
<br/>


1. Creating a new Native Block

Native blocks can be used to create blocks that you can drag and drop on to your workflows. This feature allows you to mix low-coding with NoCodeXpress workflows.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0117.png"/>

2. Coding the Native Block

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0118.png"/>

to return a response from the block you can use the “setResponse” method.

The “controller” parameter is used to access the information from the workflow that is currently being executed. 


The controller variable has the following fields;


|Field|Description|
|controller.node|Workflow node that represents the current native block|
|controller.node.config|You can use this variable to access the properties of the current native block the developer has configured|
|controller.inputs|Represents the variables that are sent to the current native block|
|controller.inputs.current|Represents the current scope|
|controller.inputs.props|This is only applicable for UI Components which you can access the properties of it|
|controller.inputs.path|You can use this variable to access the path parameters of the current page|
|controller.inputs.query|You can use this variable to access the query parameters of the current page|

You can create properties for your Native Block using the tool window “State / Properties”

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0119.png"/>

3. Using Promises in your Code


If you need to call a 3rd party API or use browser specific features such as geo location, access microphone or any other asynchronous task in your Native block, you can return a promise in the code. 

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0120.png"/>

When you use promises, you need to use the setResponse method inside the promise.

After you set the response, you need to resolve the promise to continue the execution of the workflow




4. Using the Native Block

To drag and drop the native block to your workflow, you can find it under the toolbox category “Native Blocks”. After you drag and drop the block you can change its properties in the tool window  Selected Item Properties 


<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0121.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0122.png"/>
