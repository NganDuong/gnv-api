# User Management: CHECK REGISTRATION

Use to check user's infomation before register.

**URL** : `users/check`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : NO

**Data params**

**Data example**                            

    - Kiểm tra username: /users/check?username={username}

    - Kiểm tra số điện thoại: /users/check?phone={phone}

    - Kiểm tra email: /users/check?email={email}

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "user_code": "GNV_globaladmin",
            "username": "admin",
            "email": "admin@gnv.vn",
            "phone": "0123456789",
            "role_id": 1,
            "status": 1,
            "created": "2018-03-30T20:00:00+07:00",
            "modified": "2018-03-30T20:00:00+07:00"
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found user(s)"
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