---
label: Users
order: 100000
---

## Users

All the routes about the users

### Routes

==- [!badge text="POST" variant="success"] Login

###### http://ip:port/login

All parameters need to be in a form-data.


#### Parameters
<br>


##### Body
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The account username | true |
| password | string | The account password | true |


#### Responses
<br>



| Status | Description |
| ------ | ----------- |
| 200: OK | Logged in |
| 400: Bad Request | Wrong username or password |



==- [!badge text="POST" variant="success"] Logout

###### http://ip:port/logout


#### Responses
<br>



| Status | Description |
| ------ | ----------- |
| 200: OK | Logged out |
| 400: Bad Request | You are not logged in |


==- [!badge text="POST" variant="success"] Create Account

###### http://ip:port/createAccount

All parameters need to be in a form-data.


#### Parameters
<br>


##### Body
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The account username | true |
| password | string | The account password | true |
| type | string | The account type (Admin, Adult, Teen, Kid) | true |
| profilePicture | File | The profile picture image | false |


#### Responses
<br>



| Status | Description |
| ------ | ----------- |
| 200: OK | Account created |
| 400: Bad Request | Username already exists |



==- [!badge text="POST" variant="success"] Edit Account

###### http://ip:port/profil

All parameters need to be in a form-data.


#### Parameters
<br>


##### Body
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The account username | false |
| password | string | The account password | false |
| profilePicture | File | The profile picture image | false |


#### Responses
<br>



| Status | Description |
| ------ | ----------- |
| 200: OK | Account edited |
| 400: Bad Request | You are not logged in |



==- [!badge text="GET"] Who am I ?

###### http://ip:port/whoami

You need to be logged in.

The route return in a JSON the account data, the name, the sha256 password, the profile picture, and the account type


#### Responses
<br>



| Status | Description |
| ------ | ----------- |
| 200: OK | Account data |
| 400: Bad Request | You are not logged in |

===