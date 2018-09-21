# User Management: PROFILE - FORGET PASSWORD - UPDATE

Use to update user's infomation.

**URL** : `users/forgetPassword`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
    "token": "[received token]",
    "email": "[user email]",
    "new_password": "[new password]"
}
```

**Data example**

```json
{
    "token": "lkUWPIyAlM",
    "email": "ngan.duong1995@gmail.com",
    "new_password": "123456"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "user": {
            "id": 5,
            "user_code": "G1527473478",
            "username": "customer",
            "email": "ngan.duong1995@gmail.com",
            "phone": "01234567893",
            "role_id": 6,
            "status": 1,
            "created": "2018-05-27T12:11:18+07:00",
            "modified": "2018-09-21T16:08:34+07:00"
        },
        "token": "GNV eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOjUsImV4cCI6MTUzNzYwNzMxNH0.pwr1BrwbmzYTYpg6o9rMEj11rHyLu3Y9RIkOcyLal9Y"
    },
    "paging": [],
    "message": "Your password has been changed successfully."
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
    "message": "User not found"
}
```