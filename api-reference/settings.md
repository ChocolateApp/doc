---
label: Settings
order: 99991
---

# Settings

All routes related to settings

## Routes

==- [!badge text="POST" variant="success"] Edit settings

##### http://ip:port/saveSettings/

Parameters in form data

### Parameters
<br>

#### Form data
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| language | string | The language | false |
| port | string | The port | false |
| tmdbKey | string | The tmdbApiKey | false |
| igdbSecret | string | The igdbSecret | false |
| igdbID | string | The igdbKey | false |
| allowDownloadsCheckbox | string | The allowDownloadsCheckbox (on/off) | false |

### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | Settings saved |