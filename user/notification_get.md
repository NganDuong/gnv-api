# User Management: NOTIFICATION GET

Use to get notifications of current user.

**URL** : `/users/notifications/{id}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "id": [notification's id],
    "user_id": [user's id],
    "status": [0 | 1],
    "created": "[datetime]",
}
```

**URL example**

/users/notifications?status=0

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 28,
            "notification_id": 26,
            "user_id": 2,
            "status": 0,
            "created": "2018-08-21T17:12:06+07:00",
            "modified": "2018-08-21T17:12:06+07:00",
            "order_notification": {
                "id": 26,
                "order_id": 14,
                "order_code": "O1534220134",
                "target_id": 41,
                "target_type": 1,
                "created": "2018-08-21T17:12:06+07:00",
                "modified": "2018-08-21T17:12:06+07:00",
                "header": "Sửa thông tin điểm lấy hàng",
                "content": "Lấy tại 200 Nguyễn Trãi"
            }
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found ordernotificationstatus(s)"
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
    "message": "ordernotificationstatus not found"
}
```