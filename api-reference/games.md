---
label: Games
order: 99996
---

# Games

All the routes related to games

## Routes

==- [!badge text="GET"] Get all system

##### http://ip:port/getAllConsoles/:librarieName

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
| 200: OK | All the system |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get system data

##### http://ip:port/getConsoleData/:consoleName

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| consoleName | string | The console name | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The console data |

==- [!badge text="GET"] Get all games

##### http://ip:port/getGames/:librarieName

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
| 200: OK | All the games |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get the game file

##### http://ip:port/gameFile/:console/:gameSlug

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| console | string | The console name | true |
| gameSlug | string | The game slug | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The game file |

==- [!badge text="GET"] Get the console bios

##### http://ip:port/bios/:console

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| console | string | The console name | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The console bios |

==- [!badge text="GET"] Get the game data

##### http://ip:port/getGameData/:gameId

Parameters in the path

### Parameters
<br>

#### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| gameId | string | The game id (from IGDB) | true |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The game data |
| 404: Not Found | The game was not found |

===
