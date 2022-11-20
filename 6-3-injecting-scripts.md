## 6.3. Injecting Custom Scripts
<br/>

1. Importing 3rd Party Scripts

You can also import 3rd party JavaScripts for your application using the “Frontend App” item under the “Scripts” section. 

You can prefer to either load it in design time, runtime or both. When you choose to load in design time, when you open the project through the IDE the scripts automatically gets loaded. This feature can be useful if you need to import Vue.js components, create native components and use those components in your designer.

Runtime script loading only works when you execute your application.

If you choose synchronous load, the subsequent script gets loaded only after the current scripts gets loaded. This feature is useful when it is required to load scripts with dependencies from the previous ones.

You can also choose to append the script to either header or the body of the html page of your application.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0123.png"/>


2. Loading Scripts in the Project


You can also create a script inside your project and load using the same method. First create a script, add your custom coding and inside the “Frontend App” item under “Secipts” section, you can import your document.


<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0124.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0125.png"/>

