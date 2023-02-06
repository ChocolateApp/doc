---
label: Other
order: 99993
---

## Other

All routes related to other videos

### Routes

==- [!badge text="GET"] Get all other videos

###### http://ip:port/getAllOther/:librarieName

Parameters in the path

#### Parameters
<br>

##### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| librarieName | string | The librarie name | true |

#### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | All the other videos |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get other video stream

###### http://ip:port/otherVideo/:otherHash

Parameters in the path

#### Parameters
<br>

##### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| otherHash | string | The other video hash | true |

#### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The other video stream |
| 404: Not Found | The other video was not found |

===