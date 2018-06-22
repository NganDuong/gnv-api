# Config Management: ORDER NOTE REASON - GET

Use to create order's note reason.

**URL** : `/configs/orders/notes/{id}`

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
            "name": "Wrong phone number/address",
            "require_datetime": 0,
            "created": "2018-05-28T08:07:37+00:00",
            "modified": "2018-05-28T08:07:37+00:00"
        },
        {
            "id": 2,
            "name": "Can not contact receiver (no answer)",
            "require_datetime": 0,
            "created": "2018-05-28T08:08:53+00:00",
            "modified": "2018-05-28T08:08:53+00:00"
        },
        {
            "id": 3,
            "name": "No Show",
            "require_datetime": 0,
            "created": "2018-05-28T08:09:03+00:00",
            "modified": "2018-05-28T08:09:03+00:00"
        },
        {
            "id": 4,
            "name": "Postpone",
            "require_datetime": 1,
            "created": "2018-05-28T08:09:29+00:00",
            "modified": "2018-05-28T08:09:29+00:00"
        },
        {
            "id": 5,
            "name": "Do not want to buy item",
            "require_datetime": 0,
            "created": "2018-05-28T08:09:41+00:00",
            "modified": "2018-05-28T08:09:41+00:00"
        }
    ],
    "paging": {
        "total": 5
    },
    "message": "Found ordernotereason(s)"
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
    "message": "ordernotereason not found"
}
```