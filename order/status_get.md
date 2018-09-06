# Order Management: STATUS - GET

Use to get order's status.

**URL** : `/configs/orders/status/[id]`

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
            "id": 1,
            "name": "Order Received",
            "created": "2018-05-08T10:00:00+00:00",
            "modified": "2018-05-08T10:00:00+00:00"
        },
        {
            "id": 2,
            "name": "Order Approved",
            "created": "2018-05-08T10:00:00+00:00",
            "modified": "2018-05-08T10:00:00+00:00"
        },
        {
            "id": 3,
            "name": "To Be Picked Up",
            "created": "2018-05-08T10:00:00+00:00",
            "modified": "2018-05-08T10:00:00+00:00"
        },
        {
            "id": 4,
            "name": "Picked Up",
            "created": "2018-05-08T10:00:00+00:00",
            "modified": "2018-05-08T10:00:00+00:00"
        },
        {
            "id": 5,
            "name": "Scanned/Checked",
            "created": "2018-05-08T10:00:00+00:00",
            "modified": "2018-05-08T10:00:00+00:00"
        }
    ],
    "paging": {
        "next": "/configs/orders/status?page=2",
        "total": 15
    },
    "message": "Found orderstatus(s)"
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
    "message": "orderstatus not found"
}
```