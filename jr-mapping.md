### JSON-Relational Mapping
<br/>
To easily manipulate data in a relational databases NoCodeXpress uses a paradigm known as JSON-Relational (J-R) mapping. 
<br/><br/><br/>
In JSON data is represented in a tree like structure where a parent object can have various child objects, where as in Relational databases data is represented in a graph like format with relationships among multiple entities.
<br/><br/><br/>
J-R mapping in NoCodeXpress takes a JSON first approach where the developer can define parent-child relationships and, select various database specific data types for fields in an entity. 
 <br/><br/><br/>
As a result JSON data can easily be inserted, and retrieved easily and efficiently from relational databases
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_1.png"/>
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_2.png"/>
<br/><br/><br/>
Also in NoSQL Document databases, although JSON documents can be stored and queried, data is stored with redundancy. J-R mapping approach also aims to eliminate redundancy by enabling the developers to map parent entities to child entities with an "association" relationship type.
<br/><br/><br/>

#### Defining Parent child relationships
<br/>
After you have created a relationship, you can select the relationship type from the "Relationship" drop down.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_3.png"/>
<br/><br/><br/>
In J-R mapping there are three types of relationships.
<br/><br/><br/>
1. Composition : When a parent item is inserted with the child items, each child item is assigned only to that particular parent. When a parent item is being deleted its children will also get deleted.<br/><br/>
2. Aggregation: When a parent item is inserted with the child items, each child item is assigned only to that particular parent. When a parent item is being deleted its children will NOT get deleted.<br/><br/>
3. Association: Each child item can be associated with multiple parent items. When A parent item is being inserted with child items, child items should already be there in the database. When the parent item is being deleted, its child items wont get deleted. This can be used to avoid data redundancy<br/><br/>

#### Retrieving data from MySQL
<br/>
After you have created the schema and its relationships you can use the block "Read multiple records from MySQL" to retrieve data from the database. First you have to select the schema.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_4.png"/>
<br/><br/><br/>
The configure the data you need to retrieve you can click on Field Configuration.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_5.png"/>
<br/><br/><br/>
Then the Object Constructor dialog box will pop up. After that you have to create a preset with all the field configuration for you to retrieve data. You can create a preset by selecting "[Create New]" from the drop down on the top.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_6.png"/><br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_7.png"/>
<br/><br/><br/>
After the preset is created, you can select an entity from the "Entity Name" drop down on the right side.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_8.png"/>
<br/><br/><br/>
By clicking on the "Filter" button you can add a where condition. you can also include variables too.  Similarly if you wish to sort your results you can add fields for Order By text box, and if you wish to use pagination you can add parameters to Skip and Take.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_9.png"/>
<br/><br/><br/>
You can also select a child entities and select its fields you wish to retrieve.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_10.png"/>
<br/><br/><br/>

#### Inserting and Updating
<br/>
To insert data you have to use the block "Insert records to MySQL" which is a function block that accepts an input from its previous block. In the example below, the POST body is directly inserted to MySQL. You also need to select the schema and the entity for this block. If you check "Overwrite if exists" it will insert if the inserting object with its ID already exists on the table, if not the operation will update the row with the same ID in the table.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_11.png"/>
<br/><br/><br/>
To update data you have to use the block "Update records in MySQL" with the configuration same as above.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_12.png"/>
<br/><br/><br/>

#### Deleting
<br/>
To delete a record in the database, you have to use the block "Delete a record in MySQL" which accepts a number which should be the ID of the record that should be deleted.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_13.png"/>
<br/><br/><br/>

#### Executing a Raw Query
<br/>
To execute a raw query you have to use the block "Execute a Query in MySQL". On the block properties you can select the connection settings.
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_14.png"/>
<br/><br/><br/>
This block accepts a SQL string from its previous block as shown below;
<br/><br/><br/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://nocodexpress.app/docimages/9_15.png"/>
<br/><br/><br/>