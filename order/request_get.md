# Order Management: REQUEST GET

Use to get requests of existed order.

**URL** : `/orders/requests/{id}`

**Method** : `POST`

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
            "id": 1,
            "order_id": 1,
            "creater_id": 1,
            "solver_id": 0,
            "order_request_type_id": 1,
            "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA",
            "status": 0,
            "created": "2018-05-21T08:01:55+00:00",
            "modified": "2018-05-21T08:01:55+00:00",
            "order_request_type": {
                "id": 1,
                "name": "Update order",
                "created": "2018-05-10T03:08:30+00:00",
                "modified": "2018-05-10T03:08:30+00:00"
            }
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found orderrequest(s)"
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