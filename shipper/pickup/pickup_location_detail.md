# Shipper: GET PICKUP LOCATION DETAIL

Use to get shipper's pickup location detail.

**URL** : `/orders/pickup?sender_address={address number/street}&sender_location_id={id}`

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
    "data": {
        "sender_name": "A",
        "sender_phone": "0123456789",
        "sender_address_detail": "104 NCT, Quận 1, Hồ Chí Minh",
        "sender_longitude": 0,
        "sender_latitude": 0,
        "total": 2,
        "orders": [
            {
                "id": 3,
                "cash": 40000,
                "status": "To Be Picked Up"
            },
            {
                "id": 4,
                "cash": 40000,
                "status": "To Be Picked Up"
            }
        ]
    },
    "paging": {
        "next": "/orders/pickup?sender_address=104 NCT&sender_location_id=1&page=2",
        "total": 3
    },
    "message": "Found order(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```