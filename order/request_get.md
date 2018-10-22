# Order Management: REQUEST GET

Use to get requests of existed order.

**URL** : `/orders/requests`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

**Data example**

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "order_code": "P1538367362",
            "order_id": 54,
            "total": 1,
            "requests": [
                {
                    "id": 12,
                    "order_id": 54,
                    "order_code": "P1538367362",
                    "creater_id": 5,
                    "solver_id": 1,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 1,
                    "solved": "2018-10-01T11:20:16+07:00",
                    "created": "2018-10-01T11:16:13+07:00",
                    "modified": "2018-10-01T11:20:16+07:00",
                    "solver": {
                        "username": "admin"
                    },
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    },
                    "read_status": 1
                }
            ]
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found request(s)."
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
    "message": "orderrequest not found"
}
```
