# Order Management: SEARCH

Use to search an order.

**URL** : `/orders/`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "order_code": "[order code]",
    "customer_order_code": "[customer's order code]",
    "order_status_id": [exsited status id],
    "fee_payer": [0 | 1],
    "pickup_date": "[datetime]",
    "expected_pickup_from": "[datetime]",
    
    "sender_name": "[sender's name]",
    "sender_phone": "[sender's phone number]",
    "sender_address": "[detail address (number, street)]",
    "sender_location_id": [pickup location id],

    "receiver_name": "[receiver's name]",
    "receiver_phone": "[receiver's phone number]",
    "receiver_address": "[detail address (number, street)]",
    "receiver_location_id": [delivery location id],
}
```

**URL example**

/orders?receiver[like]=ngan&order_code[like]=O1525975833&expected_pickup_from[lt]=2020

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "order_code": "O1525975833",
            "customer_order_code": "",
            "owner_id": 2,
            "warehouse_id": 0,
            "route": "Custom - [LH]BĐ.HN.Q1.[GH]Q1",
            "last_location": "",
            "current_location": "",
            "sender": "Name: Abc Asd - Phone: 0123456789 - Address: 104 NCT, Ba Đình, Hà Nội",
            "receiver": "Name: Ngân - Phone: 0123456789 - Address: 104 NCT, Quận 1, Hồ Chí Minh",
            "shipper_id": 0,
            "service_id": 1,
            "source_location_id": 4,
            "dest_location_id": 1,
            "fee_payer": 0,
            "order_status_id": 1,
            "handle_instruction": "Note",
            "coupon_code": "GC1525883032",
            "type": "ABC",
            "size": "10x10x10",
            "weight": 15,
            "value": 10000,
            "is_cod": 0,
            "cod": 0,
            "delivery_fee": 59000,
            "return_money": -49000,
            "return_method": 0,
            "pickup_date": null,
            "delivery_date": null,
            "return_date": null,
            "expected_pickup_from": "2019-01-01T19:30:00+00:00",
            "expected_pickup_to": "2019-01-02T00:00:00+00:00",
            "expected_delivery_from": "2019-01-02T00:00:00+00:00",
            "expected_delivery_to": "2019-01-02T00:00:00+00:00",
            "pickup_times": 0,
            "delivery_times": 0,
            "return_times": 0,
            "created": "2018-05-10T18:10:33+00:00",
            "modified": "2018-05-10T18:10:33+00:00",
            "order_requests": [],
            "order_notes": [],
            "pickup_photos": [],
            "barcode": {
                "id": 1,
                "target_id": 1,
                "target_type": "Orders",
                "field": "Barcode",
                "path": "/uploads/files//orders/barcodes//order_1525975833.png",
                "created": "2018-05-10T18:10:33+00:00",
                "modified": "2018-05-10T18:10:33+00:00"
            },
            "deliver_location": {
                "id": 1,
                "support_type_id": 3,
                "area_type_id": 1,
                "district_id": 1,
                "province_id": 1,
                "created": "2018-05-09T07:18:12+00:00",
                "modified": "2018-05-09T07:18:12+00:00"
            },
            "pickup_location": {
                "id": 4,
                "support_type_id": 3,
                "area_type_id": 1,
                "district_id": 6,
                "province_id": 2,
                "created": "2018-05-09T07:19:35+00:00",
                "modified": "2018-05-09T07:19:35+00:00"
            },
            "shipper": null,
            "owner": {
                "id": 2,
                "user_code": "G1525973655",
                "username": "ngan",
                "email": "ngan@abc.com",
                "phone": "01234156789",
                "address": "",
                "location_id": 2,
                "role_id": 5,
                "status": 1,
                "created": "2018-05-10T17:34:15+00:00",
                "modified": "2018-05-10T18:45:45+00:00"
            },
            "order_status": {
                "id": 1,
                "name": "Order Received",
                "created": "2018-05-08T10:00:00+00:00",
                "modified": "2018-05-08T10:00:00+00:00"
            },
            "service": {
                "id": 1,
                "name": "Same Day",
                "price": 9000,
                "created": "2018-05-09T07:30:48+00:00",
                "modified": "2018-05-09T07:30:48+00:00"
            },
            "warehouse": null
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