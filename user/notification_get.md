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
            "id": 418879,
            "notification_id": 50725,
            "user_id": 105,
            "status": 0,
            "created": "2018-12-25T14:39:14+07:00",
            "modified": "2018-12-25T14:39:14+07:00",
            "order_notification": {
                "id": 50725,
                "order_id": null,
                "order_code": "",
                "target_id": 17,
                "target_type": 3,
                "created": "2018-12-25T14:39:14+07:00",
                "modified": "2018-12-25T14:39:14+07:00",
                "order": null,
                "header": "NEW BRAND",
                "content": "new opening @ 07/11/2018",
                "reference": ""
            }
        }
    ],
    "paging": {
        "next": "/users/notifications?order_by=desc(created)&page=2",
        "total": 61,
        "total_page": 4,
        "total_read": 36
    },
    "message": "Tìm thấy ordernotificationstatus(s)"
        
```

```json
{
    "success": true,
    "data": [
        {
            "id": 193619,
            "notification_id": 20635,
            "user_id": 105,
            "status": 1,
            "created": "2018-12-08T19:17:03+07:00",
            "modified": "2018-12-08T21:14:05+07:00",
            "order_notification": {
                "id": 20635,
                "order_id": 1764,
                "order_code": "P1544201521",
                "target_id": 24027,
                "target_type": 2,
                "created": "2018-12-08T19:17:03+07:00",
                "modified": "2018-12-08T19:17:03+07:00",
                "header": "Đã giao",
                "content": "Đơn hàng được giao bởi cattuongshipper",
                "order_status_id": 16
            }
        }
    ],
    "paging": {
        "next": "/users/notifications?order_by=desc(created)&page=2",
        "total": 61,
        "total_page": 4,
        "total_read": 36
    },
    "message": "Tìm thấy ordernotificationstatus(s)"
        
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