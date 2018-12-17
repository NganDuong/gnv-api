# User Management: PROFILE - INFO - UPDATE

Use to update user's infomation.

**URL** : `users/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Optional_

```json
{
    "name": "[name]",
    "username": "[username]",
    "password": "[password in plain text]",
    "email": "[email address]",
    "phone": "[phone number]",
    "address": "[detail address (number, street)]",
    "location_id": [exsited location_id]
}
```

**Data example**

```json
{
  "location_id": 2
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 1,
        "user_code": "GNV_globaladmin",
        "username": "admin",
        "name": "name",
        "email": "admin@gnv.vn",
        "phone": "0123456789",
        "address": "104 NCT",
        "location_id": 2,
        "role_id": 1,
        "status": 1,
        "created": "2018-03-31T03:00:00+00:00",
        "modified": "2018-05-10T17:52:36+00:00"
    },
    "paging": [],
    "message": "Updated user"
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
    "message": "user not found"
}
```
OR

**Condition** : If required fields is empty or invaild.

**Code** : `409 CONFLICT`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "You are not allow to access that location"
}
```
