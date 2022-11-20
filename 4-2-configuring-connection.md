## 4.2. Configuring Database Connection
<br/>

You can configure your connection settings under the “Connection Settings” tool window. 

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0052.png"/>

On the connection settings dialog box you can configure the connection settings for each environment. You can find information about how to create environments and deploy your app in environments on a seperate cheat sheet.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0053.png"/>


If you configure your settings under “All Environments” sections. Those settings will be applied to all the other environments. 

For example, if you configure “TestDB” as the datbase name under All Environments, rest of the environments will also use “TestDB” as the database name. 

You can also overide “All Environment” settings by configuring each environment settings seperately. For example, if you configure “TestDB” as the database name under “All Environments” and if you configure “CustomerDB” under “Sandbox Development”, when your application runs in “Sandbox Deployment” it will use “CustomerDB” as the database name
