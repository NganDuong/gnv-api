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
            "id": 1,
            "order_code": "O1527474738",
            "customer_order_code": "12312312",
            "owner_id": 1,
            "warehouse_id": 0,
            "pdrs_id": 1,
            "route_id": null,
            "route_text": "Custom - [LH]Q1.Q1.[GH]Q1",
            "last_location": "",
            "current_location": "",
            "sender_name": "Ngan",
            "sender_phone": "0123456789",
            "sender_address": "104 NCT",
            "sender_location_id": 1,
            "receiver_name": "Ngân",
            "receiver_phone": "0123456789",
            "receiver_address": "104 NCT",
            "receiver_location_id": 1,
            "shipper_id": 2,
            "service_id": 1,
            "fee_payer": 1,
            "fee_paid": 0,
            "order_status_id": 3,
            "handle_instruction": "Note",
            "coupon_code": "",
            "type": "ABC",
            "size_lenght": 10,
            "size_width": 10,
            "size_height": 10,
            "weight": 10,
            "value": 50000,
            "cod": 6000,
            "prepaid": 0,
            "return_method": 1,
            "pickup_date": "2019-01-21T00:00:00+00:00",
            "delivery_date": null,
            "return_date": null,
            "expected_pickup_from": "2019-01-21T00:00:00+00:00",
            "expected_pickup_to": "2019-02-01T00:00:00+00:00",
            "expected_delivery_from": "2019-01-02T00:00:00+00:00",
            "expected_delivery_to": "2019-01-02T00:00:00+00:00",
            "pickup_times": 0,
            "delivery_times": 0,
            "return_times": 0,
            "created": "2018-05-28T02:32:18+00:00",
            "modified": "2018-05-28T04:10:45+00:00",
            "pickup_photos": [],
            "qrcode": {
                "id": 2,
                "target_id": 1,
                "target_type": "Orders",
                "field": "Qrcode",
                "path": "/uploads/files//orders/barcodes//qrcode_order_1527474738.png",
                "created": "2018-05-28T02:32:18+00:00",
                "modified": "2018-05-28T02:32:18+00:00"
            },
            "barcode": {
                "id": 1,
                "target_id": 1,
                "target_type": "Orders",
                "field": "Barcode",
                "path": "/uploads/files//orders/barcodes//barcode_order_1527474738.png",
                "created": "2018-05-28T02:32:18+00:00",
                "modified": "2018-05-28T02:32:18+00:00"
            },
            "order_status": {
                "id": 3,
                "name": "To Be Picked Up",
                "customer_display": "To Be Picked Up",
                "created": "2018-05-08T03:00:00+00:00",
                "modified": "2018-05-23T19:45:54+00:00"
            },
            "service": {
                "id": 1,
                "name": "Same Day",
                "price": 9000,
                "created": "2018-05-09T07:30:48+00:00",
                "modified": "2018-05-09T07:30:48+00:00"
            },
            "sender": "Name: Ngan - Phone: 0123456789 - Address: 104 NCT, Quận 1, Hồ Chí Minh",
            "receiver": "Name: Ngân - Phone: 0123456789 - Address: 104 NCT, Quận 1, Hồ Chí Minh",
            "size": "10x10x10",
            "delivery_fee": 34000,
            "cash": 40000,
            "return_money": 6000
        }
    ],
    "paging": [],
    "message": "Route found"
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