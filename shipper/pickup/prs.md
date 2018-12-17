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
            "owner_id": 3,
            "sender_phone": "0945015815",
            "sender_address": "103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam",
            "sender_location_id": 10,
            "sender_longitude": 106.676646,
            "sender_name": "Huyền Trang ",
            "sender_latitude": 10.76594,
            "sender_address_detail": "103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam, Quận 10, Hồ Chí Minh",
            "flag": -1,
            "total": 1,
            "total_picked_up": 1,
            "total_failed": 0,
            "orders": [
                {
                    "id": 16,
                    "order_code": "P1544777387",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 5,
                    "discount": 0,
                    "flag": -1,
                    "pickup_photos": [
                        {
                            "id": 51,
                            "target_id": 16,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/16/pickup/af5823c9-45f5-424b-a41a-3a8ce0a7912d14842163.jpg",
                            "created": "2018-12-14T15:51:40",
                            "modified": "2018-12-14T15:51:40"
                        }
                    ],
                    "cash": 0,
                    "status": "Đã Lấy",
                    "session": "Ca chiều"
                }
            ],
            "group_status_id": 5,
            "group_status": "Đã Lấy"
        },
        {
            "owner_id": 3,
            "sender_phone": "0945015815",
            "sender_address": "103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam",
            "sender_location_id": 10,
            "sender_longitude": 106.676646,
            "sender_name": "Huyền Trang ",
            "sender_latitude": 10.76594,
            "sender_address_detail": "103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam, Quận 10, Hồ Chí Minh",
            "flag": 0,
            "total": 4,
            "total_picked_up": 4,
            "total_failed": 0,
            "orders": [
                {
                    "id": 17,
                    "order_code": "P1544777389",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 5,
                    "discount": 0,
                    "flag": 0,
                    "pickup_photos": [
                        {
                            "id": 52,
                            "target_id": 17,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/17/pickup/20f1f290-ee1f-45c6-83b1-14eff14771311670418771.jpg",
                            "created": "2018-12-14T15:51:48",
                            "modified": "2018-12-14T15:51:48"
                        }
                    ],
                    "cash": 0,
                    "status": "Đã Lấy",
                    "session": "Ca chiều"
                },
                {
                    "id": 18,
                    "order_code": "P1544777390",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 5,
                    "discount": 0,
                    "flag": 0,
                    "pickup_photos": [
                        {
                            "id": 53,
                            "target_id": 18,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/18/pickup/f425238e-35ee-4b7c-bbbd-15ab840fb3821342737676.jpg",
                            "created": "2018-12-14T15:51:57",
                            "modified": "2018-12-14T15:51:57"
                        }
                    ],
                    "cash": 0,
                    "status": "Đã Lấy",
                    "session": "Ca chiều"
                },
                {
                    "id": 19,
                    "order_code": "P1544777391",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 5,
                    "discount": 0,
                    "flag": 0,
                    "pickup_photos": [
                        {
                            "id": 54,
                            "target_id": 19,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/19/pickup/e1618e9f-0f7e-4a52-aa18-325958c74ded1921040881.jpg",
                            "created": "2018-12-14T15:52:05",
                            "modified": "2018-12-14T15:52:05"
                        }
                    ],
                    "cash": 0,
                    "status": "Đã Lấy",
                    "session": "Ca chiều"
                },
                {
                    "id": 20,
                    "order_code": "P1544777392",
                    "user_code": "G1542281784",
                    "fee_paid": 0,
                    "order_status_id": 5,
                    "discount": 0,
                    "flag": 0,
                    "pickup_photos": [
                        {
                            "id": 55,
                            "target_id": 20,
                            "target_type": "Orders",
                            "field": "Pickup",
                            "path": "/uploads/files/orders/20/pickup/27c2dfca-0959-4b48-8c3a-6cc52ccbc7ce1525307469.jpg",
                            "created": "2018-12-14T15:52:12",
                            "modified": "2018-12-14T15:52:12"
                        }
                    ],
                    "cash": 0,
                    "status": "Đã Lấy",
                    "session": "Ca chiều"
                }
            ],
            "group_status_id": 5,
            "group_status": "Đã Lấy"
        }
    ],
    "paging": {
        "total": 2,
        "total_page": 1
    },
    "message": "Tìm thấy đơn hàng"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```