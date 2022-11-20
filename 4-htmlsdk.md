
# HTML 5 SDK Reference

## 1. Special Directives for HTML5 Components

 
HTML SDK allows you to create custom HTML components that can be dragged and dropped to your no-code application. You can use any available HTML tags to define the structure of your component. However, to add custom behavior, there are special Lesscode Plus directives you can insert as attributes to your HTML tags.

 This section of the documentation covers only the coding area of HTML custom components. If you would like to learn how to create Lesscode Plus custom HTML components, you can watch our crash course video.

Also note that Lesscode Plus uses  Vue.js as the underlying UI library. Therefore it uses Vue.js's template syntax to write custom components.

Following is a list of directives you can use in your custom HTML5 components.  
 
###  1.1. Control Directives

Control directives allow developers to add special behaviors through HTML attributes, and tags to their custom HTML components in Lesscode Plus. 

These directives are used in top-level tags of HTML components to make it possible to use them in the IDE and application runtime. 

When you create a custom component it's mandatory to include either 'native-html' or 'lc-component' directive in your component.

#### native-html

This attribute is used for tags available in HTML, such as div, canvas, label, etc...

```html
<canvas native-html>
</canvas>
```

#### lc-component

Lesscode Plus is 100% compatible with existing Vue.Js libraries. Therefore you can easily import a library to the IDE, create a custom component, and drag and drop it in your IDE.

This attribute can be used for 3rd party  Vue.Js components to make them work with Lesscode Plus

```html
<el-calendar lc-component v-model="lc_model">
</el-calendar>
```


### lc-children

In HTML, some tags have children such as 'div'. To allow dragging and dropping child elements and render those child elements in runtime, you can use the directive lc-children.

```html
<div  native-html>
	<lc-children/>
</div>
```


### 1.2. Property Directives

In Lesscode Plus IDE after a component is created by dragging and dropping. It will allow the developer to select it and configure its properties of it. Property directives allow you to read those developer-configured properties in your HTML component and pass the data into any child element in your component.


#### blockProps

blockProps directive enables you to use the defined properties in your component.

```html
<el-avatar 	lc-component
			:shape="blockProps.shape" 
			:size="blockProps.size" 
			:src="blockProps.src" 
			:icon="blockProps.icon">
</el-avatar>
```

#### lc_model

This directive enables you to pass a value to  Vue's v-model directive 

```html
<el-input  v-model="lc_model">
</el-input>
```


### 1.3. Method Directives

Method directives allow the developers to use special methods available in Lesscode Plus SDK. 

#### getBinding()

In Lesscode Plus, data can be bound to various properties in a component. Unlike the blockProps directive which only allows to read of a developer-defined value, getBinding() allows the developer to read the data bound to the component's property.

```html
<iframe  native-html :src="getBinding('src')">
</iframe>
```

#### handleEvent()

HTML  components and Vue components have event handlers. In a Lesscode Plus application, the events are handled using block-based micro workflows. handleEvent() method maps an event in the HTML or Vue component into a property of a component. 
When the component is dragged, dropped and created in the IDE, the developer can select that property and assign a micro workflow into it to handle the event.

```html
<el-checkbox  lc-component  @change="handleEvent('onChange')" v-model="lc_model" >
</el-checkbox>
```

#### executeCommand()

This method allows the developer to invoke various features in the Lesscode Plus runtime engine. For example, the following navigates to another page.

```html
<div  native-html  @mouseup="executeCommand('routerlink',{prop:'href'})">		
	<lc-children/>
</div>
```

### converters()

Some Vue componets require strict data types. the converters helper converts to various data types of properties. Those data types include int, float, bool, and string.

```html
<el-row  lc-component  :gutter="converters.int(blockProps.gutter)">
</el-row>
```