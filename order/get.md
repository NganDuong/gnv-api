# Order Management: GET

Use to get user's order infomation.

**URL** : `/orders/[id]`

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
            "id": 70,
            "order_code": "O1531306123",
            "customer_order_code": "123ABC",
            "owner_id": 8,
            "warehouse_id": 1,
            "pdrs_id": 103,
            "route_id": null,
            "route_text": "Custom - [LH]Q1.Q1.[GH]Q7",
            "last_location": ".",
            "current_location": "Q1.WB1531708423",
            "sender_name": "Nov.ClothingStore",
            "sender_phone": "0123456789",
            "sender_address": "226 Nguyễn Công Trứ, P. Nguyễn Thái Bình",
            "sender_location_id": 1,
            "sender_longitude": 106.698154,
            "sender_latitude": 10.767953,
            "receiver_name": "My Nguyen",
            "receiver_phone": "0168689854",
            "receiver_address": "Tòa Nhà Thiên Sơn Plaza. 800 Nguyễn Văn Linh",
            "receiver_location_id": 14,
            "receiver_longitude": 106.718239,
            "receiver_latitude": 10.732414,
            "shipper_id": 3,
            "service_id": 1,
            "fee_payer": 0,
            "fee_paid": 0,
            "order_status_id": 7,
            "handle_instruction": "Không cho thử",
            "coupon_code": "",
            "type": "Quần Áo",
            "size_lenght": 10,
            "size_width": 10,
            "size_height": 5,
            "weight": 100,
            "value": 370000,
            "cod": 370000,
            "prepaid": 0,
            "return_method": 1,
            "pickup_date": "2018-07-12T09:12:24",
            "delivery_date": null,
            "return_date": null,
            "expected_pickup_from": "2018-07-11T00:00:00",
            "expected_pickup_to": "2018-07-11T00:00:00",
            "expected_delivery_from": "2018-07-11T00:00:00",
            "expected_delivery_to": "2018-07-11T00:00:00",
            "pickup_times": 1,
            "delivery_times": 0,
            "return_times": 0,
            "created": "2018-07-11T17:48:44",
            "modified": "2018-07-16T09:35:31",
            "pickup_photos": [
                {
                    "id": 328,
                    "target_id": 70,
                    "target_type": "Orders",
                    "field": "Pickup",
                    "path": "/uploads/files/orders/pickup/e6c458e3-077c-4197-a3f3-420f72adb067358914640.jpg",
                    "created": "2018-07-12T09:12:10",
                    "modified": "2018-07-12T09:12:10"
                },
                {
                    "id": 329,
                    "target_id": 70,
                    "target_type": "Orders",
                    "field": "Pickup",
                    "path": "/uploads/files/orders/pickup/1cba9037-607a-4ac2-aed8-cef1d27b9f56598428143.jpg",
                    "created": "2018-07-12T09:12:20",
                    "modified": "2018-07-12T09:12:20"
                }
            ],
            "qrcode": {
                "id": 295,
                "target_id": 70,
                "target_type": "Orders",
                "field": "Qrcode",
                "path": "/uploads/files/orders/barcodes/qrcode_order_1531306124.png",
                "created": "2018-07-11T17:48:44",
                "modified": "2018-07-11T17:48:44"
            },
            "barcode": {
                "id": 294,
                "target_id": 70,
                "target_type": "Orders",
                "field": "Barcode",
                "path": "/uploads/files/orders/barcodes/barcode_order_1531306124.png",
                "created": "2018-07-11T17:48:44",
                "modified": "2018-07-11T17:48:44"
            },
            "order_status": {
                "id": 7,
                "name": "Ready To Deliver",
                "customer_display": "Ready To Deliver",
                "color": "#FFE047",
                "created": "2018-05-07T20:00:00",
                "modified": "2018-05-23T12:46:46"
            },
            "service": {
                "id": 1,
                "name": "Chuẩn",
                "group_location_id": 0,
                "location_type_id": 1,
                "description": "",
                "created_before": "2018-07-16T10:00:00",
                "delivery_day": 0,
                "delivery_before": "2018-07-16T18:00:00",
                "standard_weight": 3000,
                "price": 19000,
                "extra_weight": 500,
                "extra_weight_price": 3000,
                "created": "2018-07-04T11:22:00",
                "modified": "2018-07-04T11:22:00"
            },
            "sender": "Name: Nov.ClothingStore - Phone: 0123456789 - Address: 226 Nguyễn Công Trứ, P. Nguyễn Thái Bình, Quận 1, Hồ Chí Minh",
            "receiver": "Name: My Nguyen - Phone: 0168689854 - Address: Tòa Nhà Thiên Sơn Plaza. 800 Nguyễn Văn Linh, Quận 7, Hồ Chí Minh",
            "size": "10x10x5",
            "insurance_fee": 0,
            "delivery_fee": 19000,
            "cash": 389000,
            "return_money": 351000,
            "expected_pickup_date": "2018-07-11T00:00:00",
            "expected_pickup_session": "morning",
            "expected_delivery_date": "2018-07-11T00:00:00",
            "expected_delivery_session": "morning"
        }
    ],
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
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "order not found"
}
```