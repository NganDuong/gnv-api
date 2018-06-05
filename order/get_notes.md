# Order Management: GET NOTES

Use to get order's notes infomation.

**URL** : `/orders/notes/{id}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "order_id": [existed order id],
    "user_id": [existed user id],
    "order_note_reason_id": [exsited note reason id],
    "field": "[Shop | ...]",
    "description": "[content]",
    "note_date": "[datetime]",
    "created": "[datetime]",
}
```

**URL example**

/orders?order_id=1

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 4,
            "user_id": 0,
            "order_id": 1,
            "order_note_reason_id": 0,
            "field": "Shop",
            "description": "Route: R1 - [LH]Q1.Q2.[GH]Q1",
            "note_date": null,
            "created": "2018-05-21T03:08:15+00:00",
            "modified": "2018-05-21T03:08:15+00:00",
            "user": null,
            "order_note_reason": null
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found ordernote(s)"
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
    "message": "ordernote not found"
}
```