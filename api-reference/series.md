---
label: Series
order: 99997
---

# Series

All the routes related to series

## Routes

==- [!badge text="GET"] Get all series

##### http://ip:port/getAllSeries/:librarieName

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
| 200: OK | All the series |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get a serie data

##### http://ip:port/getSerieData/:serieId

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| serieId | string | The serie id (from TMDB) | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The serie data |
| 404: Not Found | The serie was not found |

### Data returned
<br>

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | string | The serie id |
| name | string | The serie name |
| originalName | string | The serie original name |
| genres | string[] | The serie genres |
| duration | string | The serie duration (hh or hh:mm or hh:mm:ss) |
| description | string | The serie description |
| cast | JSON | The serie cast |
| bandeAnnonceUrl | string | The serie bande annonce url |
| serieCoverPath | string | The serie cover path |
| banniere | string | The serie banniere |
| note | float | The serie note |
| date | string | The serie date (yyyy-mm-dd) |
| serieModifiedTime | float | The serie folder modified time |
| libraryName | string | The serie library name |
| adult | boolean | The serie adult |
| seasons | JSON | The serie seasons |

==- [!badge text="GET"] Get a season data

##### http://ip:port/getSeasonData/:seasonId

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| seasonId | string | The season id (from TMDB) | true |

### Responses

<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The season data |
| 404: Not Found | The season was not found |

### Data returned

| Name | Type | Description |
| ---- | ---- | ----------- |
| serie | int | The serie id |
| seasonId | int | The season id |
| seasonNumber | int | The season number |
| release | string | The season release date (yyyy-mm-dd) |
| episodesNumber | int | The season episodes number |
| seasonName | string | The season name |
| seasonDescription | string | The season description |
| seasonCoverPath | string | The season cover path |
| modifiedTime | float | The season folder modified time |
| numberOfEpisodesInFolder | int | The number of episodes in the season folder (only used for the scans) |
| episodes | JSON | The season episodes |

==- [!badge text="GET"] Get an episode data

##### http://ip:port/getEpisodeData/:seasonId/:episodeId

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| seasonId | string | The season id (from TMDB) | true |
| episodeId | string | The episode id (from TMDB) | true |

### Responses


| Status | Description |
| ------ | ----------- |
| 200: OK | The episode data |
| 404: Not Found | The episode was not found |

### Data returned

| Name | Type | Description |
| ---- | ---- | ----------- |
| seasonId | int | The season id |
| episodeId | int | The episode id |
| episodeName | string | The episode name |
| episodeNumber | int | The episode number |
| episodeDescription | string | The episode description |
| episodeCoverPath | string | The episode cover path |
| releaseDate | string | The episode release date (yyyy-mm-dd) |
| slug | string | The episode slug |
| introStart | float | The episode intro start timecode (default: 0.0) |
| introEnd | float | The episode intro end timecode (default: 0.0) |

===