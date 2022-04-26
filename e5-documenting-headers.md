|Header name|Description|Required|Values|
|:----------|:----------|:------:|:-----|
|`Content-Type`|Specifies the format of the photo to be uploaded.|optional|**Valid values:** image/jpeg, image/png, and image/gif. **Default:** image/jpeg.|
|`Accept`|Specifies the format of the data to be returned.|optional|**Valid values:** application/json and application/xml. **Default:** application/json.|
<br>

## Sample request
This request uploads a photo in GIF format and the return data is in JSON.
<br><br>

```curl
POST https://phantasticFoto.com/api/v1/photo  

Content-Type: image/gif
Accept: application/json
```
POST body is the image to upload.
<br><br><br>

***
Exercise 5 from this [course].  

[course]: https://www.udemy.com/course/learn-api-technical-writing-2-rest-for-writers/