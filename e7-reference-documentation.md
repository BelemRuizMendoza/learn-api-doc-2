# Upload a sound file
Uploads an audio file to the current user's profile.

## URL
POST https://api.sounddate.com/profile/sound

## Headers
|Header name|Description|Required|Values|
|:----------|:----------|:------:|:-----|
|`Bearer`|Access token.|required|See the [Authorization] section.|
|`Content-Type`|Format of the sound file to be uploaded.|optional|Either `audio/mpeg` for MP3 files or `audio/x-wav` for WAV files. **Default:** MP3.|
|`Accept`|Format of the data to be returned.|optional|Either `application/xml` or `application/json`. **Default:** JSON.|

## `POST` or `PUT` body
The sound file.  

**Note:** The sound file must be 5 minutes or shorter.

### Sample request
```
{
POST https://api.sounddate.com/profile/sound
Bearer: {access token}
Content-Type: audio/mpeg
Accept: application/json
{sound file}
}
```
## Response
|Element|Description|Type|Notes|
|:-----:|:----------|:--:|:----|
|`id`|ID of the new sound file. |integer||
|`lenght`|Duration of the new sound file.|float|**Unit:** seconds.|

### Sample response
```json
{
    "id": 8956,
    "length": 26.3
}
```
<br><br>

# Retrieve a profile's list of sound files
Retrieves a list of URLs and lenghts of the audio files uploaded to the specified user's profile.

## URL
GET https://api.sounddate.com/user/{user-id}/profile/sound  
  
Where `{user id}` is the ID of the user whose profile contains the sound files.

## Query parameters
|Parameter|Values|Description|Type|Required|Notes|
|:-------:|:---:|:----------|:--:|:------:|:----|
|`sortOrder`||Determines the order in which the sound files are to be returned.|string|optional|The following rows describe its values.|
||`mostRecent`|Sorts most recent to earliest.|string|optional|**Default value.**|
||`earliest`|Sorts earliest to most recent.|string|optional||
||`shortest`|Sorts shortest to longest.|string|optional||
||`longest`|Sorts longest to shortest.|string|optional||

## Headers
|Header name|Description|Required|Values|
|:----------|:----------|:------:|:-----|
|`Bearer`|Access token.|required|See the [Authorization] section.|
|`Accept`|Format of the data to be returned.|optional|Either `application/xml` or `application/json`. **Default:** JSON.|

## Sample request
```
GET https://api.sounddate.com/user/345354/profile/sound?sortOrder=shortest
Bearer: {access token}
Accept: application/json
```
## Response
|Element|Fields|Description|Type|Notes|
|:-----:|:------|:----------|:--:|:----|
|`soundFiles`||List of sound files information.|array|The following rows describe its fields.|
||`id`|ID of the sound file.|integer||
||`url`|Location of the sound file.|string||
||`lenght`|Duration of the sound file.|float|**Unit:** seconds.|

## Sample response
```json
{
   "soundFiles": 
   [
      {
      "id": 23456,
      "url": "https://api.sounddate.com/profile/sound/23456.mp3",
      "length": 11.2
      },
      {
      "id": 24559,
      "url": "https://api.sounddate.com/profile/sound/24559.mp3",
      "length": 19.8
      }
   ]
}
```

## Status codes and errors
The following table describes the HTTP status codes supported by this API.
|Code|Description|Notes|
|:--:|:----------|:----|
|`200`|OK|The sound file was successfully added.|
|`401`|Unauthorized|The **access token** is invalid.|
|`413`|Request Entity Too Large|The uploaded sound file is longer than 5 minutes.|
<br><br><br>
***
Exercise 7 from this [course].

[Authorization]: https://www.justafakeurl.com
[course]: https://www.udemy.com/course/learn-api-technical-writing-2-rest-for-writers/
