# Exercise 2: documenting method and URL
## Retrieve an album
Returns data about the specified collection of images:  
`GET https://phantasticfoto.com/api/v1/album/{album ID}`  
* Where `{album ID}` is the ID of the album to retrieve.

## Create an album
Creates a collection of images:  
`POST https://phantasticfoto.com/api/v1/album/`  

## Update an album
Modifies the specified collection of images:  
`PUT https://phantasticfoto.com/api/v1/album/{album ID}`  
* Where `{album ID}` is the ID of the album to update.

## Delete an album
Eliminates the specified collection of images:  
`DELETE https://phantasticfoto.com/api/v1/album/{album ID}`  
* Where `{album ID}` is the ID of the album to delete.

## Retrieve a list of all the albums
Returns a list of all the currently available albums:  
`GET https://phantasticfoto.com/api/v1/album/`  

## Print an album
Prints the specified collection of images:  
`POST https://phantasticfoto.com/api/v1/album/{album ID}/print`  
* Where `{album ID}` is the ID of the album to print.

<br><br><br>
***
Exercise 2 from this [course].  

[course]: https://www.udemy.com/course/learn-api-technical-writing-2-rest-for-writers/