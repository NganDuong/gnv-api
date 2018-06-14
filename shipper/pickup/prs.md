# Shipper: GET Current PRS

Use to get shipper's current PRS.

**URL** : `/orders/pickup`

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
            "sender_location_id": 1,
            "sender_longitude": 0,
            "sender_latitude": 0,
            "total": 12,
            "sender_address_detail": "104 NCT, Quận 1, Hồ Chí Minh",
            "orders": [
                {
                    "id": 17,
                    "order_code": "O1528106810",
                    "order_status_id": 3,
                    "pickup_photos": [
                        {
                            "id": 209,
                            "target_id": 17,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/pickup/1.png",
                            "created": "2018-06-14T10:12:38+07:00",
                            "modified": "2018-06-14T10:12:38+07:00"
                        }
                    ],
                    "cash": 40000,
                    "status": "To Be Picked Up",
                    "session": "morning"
                }
            ],
            "total_picked_up": 0
        }
    ],
    "paging": {
        "total": 2
    },
    "message": "Found PRS(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```