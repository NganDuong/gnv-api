# User Management: PROFILE - INFO - GET

Use to get user's infomation.

**URL** : `users/{id}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

**Data example**                            

    - Lấy danh sách tất cả: /users

    - Lấy danh sách Điều phối: /users?role_id=2

    - Lấy danh sách Quản kho: /users?role_id=4

    - Lấy danh sách Kế toán: /users?role_id=6

    - Lấy danh sách Shipper: /users?role_id=3

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
            "modified": "2018-03-30T20:00:00+07:00",
            "user_map": null,
            "user_warehouses": [
                "Quan 1",
                "Kho Hà Nội",
                "Kho quận 5",
                "12321312"
            ],
            "avatar": {
                "id": 17,
                "target_id": 1,
                "target_type": "Users",
                "field": "avatar",
                "path": "/uploads/files/avatar/user.png",
                "created": "2018-08-06T14:17:08+07:00",
                "modified": "2018-08-06T14:17:08+07:00"
            },
            "role": {
                "id": 1,
                "name": "admin",
                "created": "2018-05-27T19:08:43+07:00",
                "modified": "2018-05-27T19:08:43+07:00"
            }
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