# User Management: REGISTER

Use to register user with customer role.

**URL** : `users/register`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : NO

**Data params**

    - _Required_

```json
{
    "username": "[username]",
    "password": "[password in plain text]",
    "email": "[email address]",
    "phone": "[phone number]"
}
```

**Data example**

```json
{
  "username": "customer1",
  "password": "123456",
  "email": "customer1@gnv.com",
  "phone": "01234567893"
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "username": "customer1",
        "email": "customer1@gnv.com",
        "phone": "01234567893",
        "user_code": "G1525932705",
        "role_id": 5,
        "created": "2018-05-10T06:11:45+00:00",
        "modified": "2018-05-10T06:11:45+00:00",
        "id": 8
    },
    "paging": [],
    "message": "Registered user"
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
            "unique": "The provided value is invalid" | "_empty": "Please input your username"
        },
        "email": {
            "unique": "The provided value is invalid" | "_empty": "Please input your email"
        },
        "phone": {
            "unique": "The provided value is invalid" | "_empty": "Please input your phone"
        },
        "password": {
            "_empty": "Please input your password"
        }
    },
    "paging": [],
    "message": "Unable to register user"
}
```

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "Empty data"
}
```
```json
{
    "success": false,
    "data": {
        "username": "Empty"
    },
    "paging": [],
    "message": "Required input invalid"
}
```