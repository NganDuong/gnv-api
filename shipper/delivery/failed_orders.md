# Shipper: GET FAILED DELIVERY ORDERS

Use to get shipper's failed to deliver orders.

**URL** : `/orders/delivery/statistics/failed`

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
            "sender_name": "A",
            "sender_phone": "0123456789",
            "sender_address": "104 NCT",
            "sender_longitude": 0,
            "sender_latitude": 0,
            "total": 1,
            "sender_address_detail": "104 NCT, Ba Đình, Hà Nội"
        }
    ],
    "paging": [],
    "message": "Found order(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```