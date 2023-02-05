---
label: Libraries
order: 99999
---

# Libraries
All the routes about the libraries

## Routes

==- [!badge text="GET"] Create a new librarie

##### http://ip:port/createLib

All parameters need to be in a json


### Parameters
<br>


#### Body

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| libName | string | The librarie name (unique) | true |
| libPath | string | The disk path of the files | true |
| libType | string | The librarie type (movies, series, games, tv, other, books) | true |
| libUsers | string | A string with all users allowed to acced to the lib. Ex: "Bob, Paulo" | false |

### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | Librarie created |
| 400: Bad Request | Librarie already exist |

==- [!badge text="GET"] Edit a librarie

##### http://ip:port/editLib/:libName

Parameters in the path and in a json


### Parameters
<br>


#### Path
| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| libName | string | The librarie name (unique) | true |

#### Body

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| libPath | string | The disk path of the files | false |
| libType | string | The librarie type (movies, series, games, tv, other, books) | false |
| libUsers | string | A string with all users allowed to acced to the lib. Ex: "Bob, Paulo" | false |

### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | Librarie edited |
| 400: Bad Request | Librarie doesn't exist |

==- [!badge text="GET"] Delete a librarie

##### http://ip:port/deleteLib/:libName

Parameters in the path


### Parameters
<br>


### Path
| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| libName | string | The librarie name (unique) | true |

### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | Librarie deleted |
| 400: Bad Request | Librarie doesn't exist |

==- [!badge text="GET"] Get all the libraries

##### http://ip:port/getAllLibraries

No parameters



### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | All the libraries |

==- [!badge text="GET"] Get all the libraries of a user

##### http://ip:port/getAllLibraries/:userName

Parameters in the path


### Parameters
<br>


### Path
| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| userName | string | The user name | true |

### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | All the libraries of the user |

==- [!badge text="GET"] Get all the libraries of a type

##### http://ip:port/getAllLibraries/:libType

Parameters in the path


### Parameters
<br>


### Path
| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| libType | string | The librarie type (movies, series, games, tv, other, books) | true |

### Parameters
<br>


| Status | Description |
| ------ | ----------- |
| 200: OK | All the libraries of the type |

===