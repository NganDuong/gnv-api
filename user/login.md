# User Management: LOGIN

Use to log an existed user in.

**URL** : `users/login`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : NO

**Data params**

    - _Required_

```json
{
    "username": "[username]",
    "password": "[password in plain text]"
}
```

**Data example**

```json
{
    "username": "shipper",
    "password": "password"
}
```

```bash
curl -X POST http://api.gnv.findsoft.vn/users/login -i -H "Content-Type: application/json" -d '{"username":"shipper","password":"123456"}'
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "user": {
            "id": 3,
            "user_code": "G1543287056",
            "name": "",
            "username": "shipper",
            "email": "shipper@mail.com",
            "phone": "06666666666",
            "address": "",
            "role_id": 3,
            "status": 1,
            "created": "2018-11-27T02:50:56+07:00",
            "modified": "2018-11-27T02:50:56+07:00",
            "avatar": null,
            "role": {
                "id": 3,
                "name": "shipper",
                "created": "2018-05-27T12:09:27+07:00",
                "modified": "2018-05-27T12:09:27+07:00"
            }
        },
        "token": "GNV eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOjMsImV4cCI6MTU0NTExNDI3N30.Q8vt0w0GqcdCQjocYrV3eYOn8b-dGGhYWlN5XBSzmX8"
    },
    "paging": [],
    "message": "Đăng nhập thành công"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `401 UNAUTHORIZED`

**Content** :

```json
{
    "success": false,
    "data": [],
    "message": "Username or password incorrect"
}
```