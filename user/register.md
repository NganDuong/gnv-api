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
    "name": "[name]",
    "password": "[password in plain text]",
    "email": "[email address]",
    "phone": "[phone number]"
}
```

**Data example**

```json
{
  "username": "ngan",
  "name": "ngan duong",
  "password": "123456",
  "email": "ngan.duong@mail.com",
  "phone": "009757454636"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [],
    "paging": [],
    "message": "An activation email has been sent to ngan.duong@mail.com"
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
