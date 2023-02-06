---
label: Books
order: 99994
---

## Books

All routes related to books

### Routes

==- [!badge text="GET"] Get all books

###### http://ip:port/getAllBooks/:librarieName

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
| 200: OK | All the books |
| 404: Not Found | The librarie was not found |

==- [!badge text="GET"] Get a book slug

###### http://ip:port/bookUrl/:bookId

Parameters in the path

#### Parameters
<br>

##### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| bookId | int | The book id | true |

#### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The book slug |
| 404: Not Found | The book was not found |

==- [!badge text="GET"] Get a book page

###### http://ip:port/bookUrl/:bookId/:page

Parameters in the path

#### Parameters
<br>

##### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| bookId | int | The book id | true |
| page | int | The page number | true |

#### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The book page |
| 404: Not Found | The book was not found |

==- [!badge text="GET"] Get a book data

###### http://ip:port/bookData/:bookId

Parameters in the path

#### Parameters
<br>

##### Path
<br>

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| bookId | int | The book id | true |

#### Responses
<br>

| Status | Description |
| ------ | ----------- |
| 200: OK | The book data |
| 404: Not Found | The book was not found |

===