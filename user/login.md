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
            "id": 1,
            "user_code": "GNV_globaladmin",
            "username": "admin",
            "email": "admin@gnv.vn",
            "phone": "0123456789",
            "address": "104 NCT",
            "location_id": 1,
            "role_id": 1,
            "status": 1,
            "created": "2018-03-31T10:00:00+00:00",
            "modified": "2018-03-31T10:00:00+00:00",
            "avatar": {
                "id": 13,
                "target_id": 1,
                "target_type": "Users",
                "field": "avatar",
                "path": "/home/nganduong/Projects/gnv-api/webroot/uploads/files//avatar/1.png",
                "created": "2018-05-04T10:45:33+00:00",
                "modified": "2018-05-04T11:01:01+00:00"
            },
            "location": {
                "id": 1,
                "support_type_id": 3,
                "area_type_id": 1,
                "district_id": 1,
                "province_id": 1,
                "created": "2018-05-07T08:26:54+00:00",
                "modified": "2018-05-08T06:15:51+00:00"
            },
            "role": {
                "id": 1,
                "name": "admin",
                "created": "2018-05-08T08:02:55+00:00",
                "modified": "2018-05-08T08:02:55+00:00"
            }
        },
        "token": "Token"
    },
    "paging": [],
    "message": "Login success"
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