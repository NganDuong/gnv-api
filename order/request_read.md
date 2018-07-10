# Order Management: READ A REQUEST

Use to update request's status to read.

**URL** : `/orders/requests/{id}`

**Method** : `PATCH`

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
    "data": {
        "id": 5,
        "order_request_id": 55,
        "user_id": 1,
        "read_status": 1,
        "created": "2018-06-11T04:48:38+00:00",
        "modified": "2018-06-11T04:58:17+00:00"
    },
    "paging": [],
    "message": "Updated orderrequest"
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