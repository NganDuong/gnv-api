# Shipper: GET Current DRS

Use to get shipper's current DRS.

**URL** : `/orders/delivery`

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
            "receiver_name": "B",
            "receiver_phone": "0123456789",
            "receiver_address": "104 NCT",
            "receiver_location_id": 1,
            "receiver_longitude": 0,
            "receiver_latitude": 0,
            "total": 1,
            "receiver_address_detail": "104 NCT, Quận 1, Hồ Chí Minh",
            "orders": [
                {
                    "id": 7,
                    "order_code": "O1528100633",
                    "cash": 6000,
                    "status": "Delivered",
                    "session": "morning"
                }
            ],
            "total_delivered": 1
        }
    ],
    "paging": [],
    "message": "Found DRS(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```