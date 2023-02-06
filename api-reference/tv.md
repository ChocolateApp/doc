---
label: TV
order: 99995
---

## TV

All the routes related to TV Channels

### Routes

==- [!badge text="GET"] Get all TV Channels

###### http://ip:port/getChannels/:librarieName

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
| 200: OK | All the TV Channels |
| 404: Not Found | The librarie was not found |

#### Data returned

```json
[
    {
        "name": name,
        "url": url,
        "channelID": channelID,
        "id": id,
        "logo": logo
    },
    ...
]
```

===