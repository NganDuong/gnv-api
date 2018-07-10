# Order Management: REQUEST STATUS GET

Use to get requests of existed order.

**URL** : `/orders/requests/status?read_status={0 | 1}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

**Data example**

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 2,
            "order_request_id": 9,
            "user_id": 3,
            "read_status": 0,
            "created": "2018-06-11T05:13:59+07:00",
            "modified": "2018-06-11T05:13:59+07:00",
            "order_request": {
                "id": 9,
                "order_id": 7,
                "creater_id": 1,
                "solver_id": 0,
                "order_request_type_id": 1,
                "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA",
                "status": 0,
                "created": "2018-06-11T05:13:59+07:00",
                "modified": "2018-06-11T05:13:59+07:00"
            }
        },
        {
            "id": 13,
            "order_request_id": 10,
            "user_id": 3,
            "read_status": 0,
            "created": "2018-06-11T11:00:01+07:00",
            "modified": "2018-06-11T11:00:01+07:00",
            "order_request": {
                "id": 10,
                "order_id": 7,
                "creater_id": 1,
                "solver_id": 0,
                "order_request_type_id": 1,
                "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA",
                "status": 0,
                "created": "2018-06-11T11:00:01+07:00",
                "modified": "2018-06-11T11:00:01+07:00"
            }
        },
        {
            "id": 16,
            "order_request_id": 11,
            "user_id": 3,
            "read_status": 0,
            "created": "2018-06-11T11:00:34+07:00",
            "modified": "2018-06-11T11:00:34+07:00",
            "order_request": {
                "id": 11,
                "order_id": 7,
                "creater_id": 1,
                "solver_id": 0,
                "order_request_type_id": 1,
                "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA",
                "status": 0,
                "created": "2018-06-11T11:00:34+07:00",
                "modified": "2018-06-11T11:00:34+07:00"
            }
        }
    ],
    "paging": {
        "next": "/orders/requests/status?read_status=0&page=2",
        "total": 14
    },
    "message": "Found orderrequeststatus(s)"
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
    "message": "orderrequeststatus not found"
}
```