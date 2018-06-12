# Shipper: GET DELIVERY LOCATION DETAIL

Use to get shipper's delivery location detail.

**URL** : `?receiver_address={address number/street}&receiver_location_id={id}&receiver_phone={phone number}`

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
        "receiver_name": "B",
        "receiver_phone": "0123456789",
        "receiver_address_detail": "104 NCT, Quận 1, Hồ Chí Minh",
        "receiver_longitude": 0,
        "receiver_latitude": 0,
        "total": 1,
        "orders": [
            {
                "id": 7,
                "order_code": "O1528100633",
                "cash": 6000,
                "status": "Delivered",
                "session": "morning"
            }
        ]
    },
    "paging": {
        "total": 1
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