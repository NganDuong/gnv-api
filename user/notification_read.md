# User Management: READ A NOTIFICATION

Use to update a notification's status to read.

**URL** : `/users/notifications/read/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**
    - _Optional_

```json
{
  "ids": [array of notification ids],
}
```

**Data example**

## Success Response

**Code** : `204 NO CONTENT`

**Content example**

```json
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "ordernotificationstatus not found"
}
```