---
label: Movies
order: 99998
---

# Movies

All the routes related to movies

## Routes

==- [!badge text="GET"] Get all movies

##### http://ip:port/getAllMovies/:librarieName

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| librarieName | string | The librarie name | true |

### Responses

<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | All the movies |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get a movie data

##### http://ip:port/getMovieData/:movieId

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| movieId | string | The movie id | true |

### Responses

<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The movie data |
| 404: Not Found | The movie was not found |

### Data returned

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | int | The movie id |
| title | string | The movie title in the folder |
| realTitle | string | The movie title in the database |
| cover | string | The movie cover |
| banner | string | The movie banner |
| slug | string | The movie slug |
| description | string | The movie description |
| note | int | The movie note |
| date | string | The movie date (dd/mm/yyyy) |
| genre | JSON | The movie genres |
| duration | strin | The movie duration (hh:mm:ss) |
| cast | JSON | The movie cast |
| bandeAnnonceUrl | string | The movie trailer url |
| adult | boolean | The movie adult |
| libraryName | string | The movie library name |
| alternativeNames | string | The movie alternative names |
| vues | JSON | The movie views {"username": timecode} |

==- [!badge text="POST" variant="success"] Set movie view timecode

##### http://ip:port/setVuesTimeCode

Parameters in the body

### Parameters
<br>

#### Body
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| movieID | int | The movie id | true |
| timeCode | int | The movie timecode | true |

### Responses

<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The movie timecode was set |
| 404: Not Found | The movie was not found |

===