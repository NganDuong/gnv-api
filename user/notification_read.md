# User Management: READ A NOTIFICATION

Use to update a notification's status to read.

**URL** : `/users/notifications/read/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

**Data example**

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 144,
        "notification_id": 67,
        "user_id": 5,
        "status": 1,
        "created": "2018-08-22T15:28:52+07:00",
        "modified": "2018-08-22T15:54:19+07:00"
    },
    "paging": [],
    "message": "Updated ordernotificationstatus"
}
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