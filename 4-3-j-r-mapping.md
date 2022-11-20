## 4.3. Entity Relationships with J-R (Json-Relational) Mapping
<br/>

With J-R Mapping you can easily map relational database tables to JSON structures. That way you can easily Create, Read and Update JSON objecs in Relational Database Tables. At this point of development only MySQL is supported. 

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0054.png"/>

To create a relationship between two entities, first select the parent entity. Create a new field to represent the relationship. And select the child entity name as the data type.

In this example to represent the relationship (One customer has many invoices). The customer entity is selected as the parent entity, and Invoice is selected as the child entity.

To create a many to one relationship

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0055.png"/>


6. Relationship types in J-R Mapping

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0056.png"/>

Association (reference): Creates a link from one object to another.

Aggregation (has-a): Creates a parent child relationship, where the child objects can exist even when the parent object is deleted.


Composition  (has-a + whole-part): Creates a parent child relationship where child objects cannot exist when the parent object is deleted. In NoCodeXpress when this type of a relationship is applied, when the parent object gets deleted its child objects also get deleted.


When you create parent child relationships with various settings in NoCodeXpress, those settings will be applied as relational database relationships in the database between tables.

|Child Relationship Type|Is Array|Relationship created in DB|
|Composition|Yes|One to Many|
|Composition|No|One to One|
|Aggregation|Yes|One to Many|
|Aggregation|No|One to Many|
|Association|Yes|Many to Many|
|Association|No|Many to One|


NoCodeXpress automatically creates the database structure in the dtabase with  the above relationships.
