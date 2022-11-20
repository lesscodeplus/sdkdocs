### Getting Started with the IDE
<br/>
After you sign up or sign in, NoCodeXpress automatically navigates to the document management page which lists all yous API projects.  
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_1.png"/>
<br/><br/><br/>
To open an existing API you can click on an existing API project, or you can also create a new API project by clicking on "New Project".
<br/><br/><br/>
After you click on "New Project" it will ask you to select a template for your API. You can select "Blank REST API" and fill in the following information;
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_2.png"/>
<br/><br/><br/>

+ Title: the name of the API
+ Description: A description of the API
+ Resource Name (Optional): REST Apis are usually used to manage a particular resource type such as a customer, order, etc.. If your API is used to manage a single resource, you can type a resource name
+ Version: the version of the API

<br/>
After you click on the "Create" button NoCodeXpress will navigate to the IDE
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_3.png"/>
<br/><br/><br/>
As you can see there are two default items on the left panel which are "All Requests" and Sandbox Deployment. Under the "All Requests" item you can specify the logic that are common to all the endpoints. Also you can modify your API details you have entered when you created your API. All Requests item is commonly used to handle tasks such as Authentication using JWT which are common to all the endpoints.
<br/><br/><br/>
Sandbox Deployment is used to run any deployment logic for your endpoints such as creating database tables on the database.  This is of the type Admin Workflow. You can also create more Admin workflows to handle tasks that should run in your back end.
<br/><br/><br/>
To create a new endpoint you can click on the "Create Item" toolbar button.
<br/><br/><br/>
<img style="max-width:45%; height:auto;" class="hovarable" src="https://nocodexpress.app/docimages/1_4.png"/>
<br/><br/><br/>
Then when you select "Endpoint" NoCodeXpress will ask for the following information.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_5.png"/>
<br/><br/>

+ Method: The request method for the new API (GET, POST, PUT, DELETE, or PATCH)
+ Path: The path for the endpoint
+ Description (Optional): The description of the API. This is used for documentation purposes
+ Summary (Optional): This is used for documentation purposes

<br/>
After you create the new endpoint, click on the "Flow" block category and select the "Set Response" block. and replace {{reference}} with "Hello World" and put it inside "Request Handling Logic"
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_6.png"/>
<br/><br/><br/>
Next, to run it make sure you have downloaded NoCodeXpress engine and running it in your local machine
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_7.png"/>
<br/><br/><br/>
Navigate to "Deploy API" and Test your connection 
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_8.png"/>
<br/><br/><br/>
Then navigate back to the API editor and click on "Run by selecting a configuration"
<br/><br/><br/>
<img style="max-width:50%; height:auto" class="hovarable" src="https://nocodexpress.app/docimages/1_9.png"/>
<br/><br/><br/>
The response of your endpoint will be shown on under the "Execution" panel on the right side.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/1_10.png"/>