# Order Management: REQUEST GET

Use to get requests of existed user.

**URL** : `/orders/requests/`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "id": [request id],
    "order_code": "[order code]",
    "order_id": [order_id],
    "status": [0 | 1],
    "creater_id": [creater_id],
    "solver_id": [solver_id],
    "order_request_type_id": [order_request_type_id],
    "created": "[datetime]",
    "solved": "[datetime]"
}
```

**URL example**

/orders/requests?order_id=8

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "order_code": "O1534220153",
            "order_id": 15,
            "total": 6,
            "requests": [
                {
                    "id": 56,
                    "order_id": 15,
                    "order_code": "O1534220153",
                    "creater_id": 5,
                    "solver_id": 0,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 0,
                    "solved": null,
                    "created": "2018-08-23T09:49:06+07:00",
                    "modified": "2018-08-23T09:49:06+07:00",
                    "solver": null,
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    }
                },
                {
                    "id": 55,
                    "order_id": 15,
                    "order_code": "O1534220153",
                    "creater_id": 5,
                    "solver_id": 0,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 0,
                    "solved": null,
                    "created": "2018-08-23T09:48:04+07:00",
                    "modified": "2018-08-23T09:48:04+07:00",
                    "solver": null,
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    }
                },
                {
                    "id": 54,
                    "order_id": 15,
                    "order_code": "O1534220153",
                    "creater_id": 5,
                    "solver_id": 0,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 0,
                    "solved": null,
                    "created": "2018-08-23T09:46:25+07:00",
                    "modified": "2018-08-23T09:46:25+07:00",
                    "solver": null,
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    }
                },
                {
                    "id": 53,
                    "order_id": 15,
                    "order_code": "O1534220153",
                    "creater_id": 5,
                    "solver_id": 0,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 0,
                    "solved": null,
                    "created": "2018-08-22T18:28:21+07:00",
                    "modified": "2018-08-22T18:28:21+07:00",
                    "solver": null,
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    }
                },
                {
                    "id": 52,
                    "order_id": 15,
                    "order_code": "O1534220153",
                    "creater_id": 5,
                    "solver_id": 0,
                    "order_request_type_id": 2,
                    "description": "Lấy tại 200 Nguyễn Trãi",
                    "status": 0,
                    "solved": null,
                    "created": "2018-08-22T18:27:15+07:00",
                    "modified": "2018-08-22T18:27:15+07:00",
                    "solver": null,
                    "order_request_type": {
                        "name": "Sửa thông tin điểm lấy hàng"
                    }
                }
            ]
        }
    ],
    "paging": {
        "next": "/orders/requests?order_id=15&page=2",
        "total": 6,
        "total_page": 2
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