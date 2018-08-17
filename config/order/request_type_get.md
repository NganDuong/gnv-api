# Config Management: REQUEST TYPE CREATE

Use to create a request's type.

**URL** : `/configs/orders/requests/{id}`

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
            "name": "Update order",
            "created": "2018-05-27T14:02:31+00:00",
            "modified": "2018-05-27T14:02:31+00:00",
            "order_requests": []
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found orderrequesttype(s)"
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
    "message": "orderrequesttype not found"
}
```