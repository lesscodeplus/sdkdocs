## 4.4. Updating Database Structure from Diagrams
<br/>


After you create the schema you need to apply the changes to the database. To do that you need to execute an Admin Workflow. In NoCodeXpress admin workflows can be used to run application maintainence related tasks. By default API projects include a default Admin Workflow - “Sandbox Deployment”

To create the database, select the admin workflow, and add the block “Update MySQL Schema” inside the trigger “When Request is Handled”

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0057.png"/>

The block “Update MySQL Schema” can be found in the toolbar category “My SQL”. You can also find blocks to insert, update, delete and to retrieve data.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0058.png"/>

To run the admin workflow click on “Run Selected API”

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0059.png"/>
