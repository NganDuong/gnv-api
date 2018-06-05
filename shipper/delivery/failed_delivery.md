# Shipper: CONFIRM FAILED TO DELIVER AN ORDER

Use to confirm failed to deliver an order.

**URL** : `/orders/delivery/failed/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**
    - _Required_

```json
{
    "order_note_reason_id": [existed reason id],
    "note": "[note]",
}
```
	- _Optional_

```json
{
    "note_date": "[datetime]",
}
```

**Data example**

```json
{
  "order_note_reason_id": 1,
  "note_date": "30/05/2018",
  "note": "dasfasfasfasf"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "success": true,
        "data": {
            "user_id": 3,
            "order_id": 2,
            "order_note_reason_id": 1,
            "field": "Failed To Deliver",
            "description": "Do not want to buy item",
            "note_date": "2018/05/30 00:00:00",
            "note": "dasfasfasfasf",
            "created": "2018-06-03T18:57:21+00:00",
            "modified": "2018-06-03T18:57:21+00:00",
            "id": 52
        },
        "paging": [],
        "message": "Note created"
    },
    "paging": [],
    "message": "Confirm failed"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```