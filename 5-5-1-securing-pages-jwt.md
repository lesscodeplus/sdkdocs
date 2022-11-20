## 5.5.1. Securing Pages with JWT
<br/>

You can also secure your UIs with JWT. To perform a token validation and cancel the navigation, add a event handler to the page’s Before Navigate event. 

Assuming the token is stored in Local Storage, you can retrieve the token using the block “Get Local Storage Item” and to perform the validation you can use the block “And Validate JWT”.

If the validation fails you can use the block “Cancel Navigation” to prevent the navigation to the page.

<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0102.png"/>
<img style="max-width:700px;max-height:350px" class="hovarable" src="https://less-code-archive.sgp1.cdn.digitaloceanspaces.com/docimages/new/0103.png"/>
