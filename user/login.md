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
    "username": "admin",
    "password": "password"
}
```

```bash
curl -X POST http://giaonhanviet.local:8080/users/login -i -H "Content-Type: application/json" -d '{"username":"admin","password":"123456"}'
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
            "user_code": "G1542189837",
            "username": "ngancustomer",
            "name": "ng,
            "email": "ngan.duong199521@gmail.com",
            "phone": "0325689741",
            "address": "",
            "role_id": 6,
            "status": 1,
            "created": "2018-11-14T17:03:57",
            "modified": "2018-11-14T17:03:57",
            "user_group_details": [],
            "avatar": null,
            "role": {
                "id": 6,
                "name": "customer",
                "created": "2018-05-27T19:09:44",
                "modified": "2018-05-27T19:09:44"
            }
        },
        "token": "GNV eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOjMsImV4cCI6MTU0MjQ0MzcxOH0.w_EyEiKufLMlYW5eUDGjFUEMWMfP666J57g1yvHWCkg"
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
