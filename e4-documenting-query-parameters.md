# Exercise 4: Documenting Query Parameters
|Parameter|Description|Type|Required|Notes|
|:-------:|:----------|:--:|:------:|:----|
|`startDate`|Considering bug detection dates, since which date to start retrieving bug data.|date|optional|**Format:** YYYY-MM-DD. **Default:** Date of the earliest bug log.|
|`endDate`|Considering bug detection dates, up to which date to stop retrieving bug data.|date|optional|**Format:** YYYY-MM-DD. **Default:** Date of the request.|
|`priority`|Determines how important the bug is.|integer|optional|**Scale:** 1 to 4, where 1 is the highest priority. **Default:** Retrieves bugs of all priorities.|
|`severity`|Determines how critical the impact of the bug is.|integer|optional|**Scale:** 1 to 4, where 1 is the highest severity. **Default:** Retrieves bugs of all severities.|
|`status`|The current status of the bug.|string|optional|**Valid values:** `open`, `closed`, `duplicate`, `notabug`. **Default:** Retrieves bugs of all statuses.|
|`start`|Index starting point of the bugs to return.|integer|optional|**Default:** Zero, the first and earliest bug on the list.|
|`total`|Total number of bugs to return after applying the request's query parameters (if any).|integer|optional|**Default:** Total number of bugs logged.|
<br><br><br>

***
Exercise 4 from this [course].

[course]: https://www.udemy.com/course/learn-api-technical-writing-2-rest-for-writers/
