---
label: Search
order: 99992
---

# Search

All routes related to search

## Routes

==- [!badge text="GET"] Search a movie

##### http://ip:port/searchInMovies/:librarieName/:search

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| librarieName | string | The librarie name | true |
| search | string | The search | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The search result |

==- [!badge text="GET"] Search a serie

##### http://ip:port/searchInSeries/:librarieName/:search

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| librarieName | string | The librarie name | true |
| search | string | The search | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The search result |

==- [!badge text="GET"] Search a book

##### http://ip:port/searchInBooks/:librarieName/:search

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| librarieName | string | The librarie name | true |
| search | string | The search | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The search result |

===