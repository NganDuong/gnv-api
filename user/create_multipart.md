# User Management: CREATE

Use to create an user.

**URL** : `users/`

**Method** : `POST`

**Content-Type** : multipart/form-data

**Auth required** : YES

**Data params**

    - _Required_

```json
{
    "username": "[username]",
    "password": "[password in plain text]",
    "email": "[email address]",
    "phone": "[phone number]",
    "role_id": [existed role_id]
}
```

    - _Optional_

```json
{
    "photo": image,
    "warehouse_id": [warehouse_id],
}
```

**Data example**

```json
{
  "username": "dispatcher",
  "password": "123456",
  "email": "dispatcher@gnv.com",
  "phone": "01234567891",
  "role_id": 2
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "username": "dispatcher",
        "email": "dispatcher@gnv.com",
        "phone": "01234567891",
        "role_id": 2,
        "user_id": 1,
        "user_code": "G1526203523",
        "created": "2018-05-13T09:25:23+00:00",
        "modified": "2018-05-13T09:25:23+00:00",
        "id": 3
    },
    "paging": [],
    "message": "Created user"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `409 CONFLICT`

**Content** :

```json
{
    "success": false,
    "data": {
        "username": {
            "unique": "The provided value is invalid"
        },
        "email": {
            "unique": "The provided value is invalid"
        },
        "phone": {
            "unique": "The provided value is invalid"
        }
    },
    "paging": [],
    "message": "Unable to create user"
}
```

OR

**Condition** : If user's role not allowed.

**Code** : `403 FORBIDDEN`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "You do not have permission for this feature"
}
```