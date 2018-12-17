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
            "owner_id": 2,
            "receiver_phone": "05614981981",
            "receiver_address": "178/8M Điện Biên Phủ, Phường 21, Bình Thạnh, Hồ Chí Minh, Việt Nam",
            "receiver_location_id": 21,
            "receiver_longitude": 106.713325,
            "receiver_name": "mi",
            "receiver_latitude": 10.800436,
            "receiver_address_detail": "178/8M Điện Biên Phủ, Phường 21, Bình Thạnh, Hồ Chí Minh, Việt Nam",
            "flag": 1,
            "total": 1,
            "total_delivered": 0,
            "total_failed": 0,
            "orders": [
                {
                    "id": 1,
                    "order_code": "P1544498831",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 7,
                    "discount": 0,
                    "flag": 1,
                    "delivery_photos": [],
                    "cod_fee": 0,
                    "return_fee": 0,
                    "service_fee": 20000,
                    "cash": 120000,
                    "status": "Chuẩn bị giao",
                    "session": "Ca chiều"
                }
            ],
            "group_status_id": 7,
            "group_status": "Chuẩn bị giao"
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found orders"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```