
# JavaScript SDK Reference

  
You can develop your custom block for your front end using JavaScript. This section only covers the JavaScript API  available in the SDK. To learn how to create your custom blocks using JavaScript you can watch our crash course video.

When you create a custom block in JavaScript it will add the following lines of code in to your block by default.

```javascript

function  execute(controller){

}

```
The function only has one parameter 'controller' that enables you to take control of the block based micro workflow.
  

## Attributes in 'controller'

Controller is an object which has many attributes, as follows;

  ```javascript

function  execute(controller){
	const {blueprint, mainVue, uiId, uIcontainer, inputs, node} = controller;
}

```

### blueprint

Lesscode Plus compiles the no-code application to a blueprint format which consists of all the UI pages, Ui Components, their events, JavaScript/CSS/HTML codes, etc... Using the blueprint key you can access all the application's resources.


### mainVue

Lesscode Plus's runtime engine renders the UI on the browser using the blueprint, and executes the events on the UI. Its developped using Vue. 'mainVue' attribute allows you to access the 'vue' object on the application level. This helps you to use the features available in Vue.js.

  ```javascript

function  execute(controller){
	const {mainVue} = controller;
	mainVue.$nextTick(()=>{
		mainVue.$set(controller.inputs.customer,"phone","123456789");
	})
	
}

```

### uiId

using this attribute you can retrieve the id number used by Lesscode Plus for the current UI page rendered on the browser.

### uiContainer

Using this attribute, you can retrieve the uiContainer that manages the state and execution of the Lesscode Plus application. You can invoke various events and listen to various events that happen in the Lesscode Plus application.

  ```javascript

function  execute(controller){
	const {uiContainer} = controller;
	//you can trigger container specific events
	uiContainer.triggerAppEvent('onError', {message:"custom error message"});
	//you can also navigate to a page
	uiContainer.navigateToUiPage({uiId:"123"});
}

```

### inputs

This parameter allows you to access the variables available in the block-based micro workflow.

  ```javascript

function  execute(controller){
	const {inputs} = controller;
	const {scope,current,rootScope,props,path,query} = inputs;
}

```

##### scope, current

These two attributes are an alias for each other. Using these attributes you can get the state variables of the UI page or UI component. Also you can create new state variables programmatically using this.

##### rootScope

This attribute allows you to get the application-level state. You can add new variables and retrieve existing variables using this attribute.

##### props

UI components allow you to define properties. the 'props' attribute allows you to access the values of the properties of the UI component.

##### path

This attribute allows you to access the path parameters (or routing parameters) sent to the UI page.

##### query

using the 'query' attribute you can access the query parameters on the browser address bar.


#### node

The 'node' object represents the currently executing block in the block-based micro workflow. 

  ```javascript

function  execute(controller){
	const {node} = controller;
	const {urn,config} = node;
}

```

##### urn

Retrieves the unique ID of the block type.

##### config
 
 Custom blocks allow you to define properties to it. using this parameter, you can access the values assigned to those properties.
  

## SDK Function

The following functions are available in the SDK.
  
#### setResponse()

Using this method, you can return a value from the custom block. custom blocks are asynchronous by default. For example, you can also run an asynchronous code, such as calling a REST API and use this method to return its data.

  ```javascript

function  execute(controller){
	setResponse(controller,"Hello World!");
}

```

#### getTemplatedValue()

As mentioned before, properties can be defined in custom JavaScript blocks. In block-based micro workflows, when the custom block is being used, variables available in the workflow can be assigned to a property of the custom block.

using this method, you can get the property's value based on the variable assigned to its property.

  ```javascript

function  execute(controller){
	const {node,inputs} = controller;
	const {config} = node;
	const propertyValue = getTemplatedValue(config,"property", inputs);
}

```

#### getTemplatedAndConvertedValue()

Similar to the above method, this method converts the value to a particular data type such as int, float, bool, or string.

  ```javascript

function  execute(controller){
	const {node,inputs} = controller;
	const {config} = node;
const  from = getTemplatedAndConvertedValue(DATA_TYPES.INT,config,"from",inputs);
}

```
