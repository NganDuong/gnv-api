# User Management: PROFILE - PASSWORD - UPDATE

Use to update user's infomation.

**URL** : `users/updatePassword`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
    "old_password": "[password]",
    "new_password": "[new password]",
    "confirm_password": "[confirm new password]"
}
```

**Data example**

```json
{
    "old_password": "1234561",
    "new_password": "123456",
    "confirm_password": "1234561"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 5,
        "user_code": "G1527473478",
        "username": "customer",
        "email": "newemail@mail.com",
        "phone": "01234567893",
        "role_id": 6,
        "status": 1,
        "created": "2018-05-27T12:11:18+07:00",
        "modified": "2018-09-21T14:30:40+07:00"
    },
    "paging": [],
    "message": "Your password has been changed successfully."
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "success": false,
    "data": {
        "confirm_password": {
            "matching": "Not matched"
        }
    },
    "paging": [],
    "message": "Confirm password not matched"
}
```