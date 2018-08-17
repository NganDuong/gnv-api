# Order Management: CREATE

Use to create an order.

**URL** : `/orders`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
  "sender_name": "[sender's name]",
  "sender_phone": "[sender's phone number]",
  "sender_address": "[detail address (number, street)]",
  "sender_location_id": [pickup location id],

  "receiver_name": "[receiver's name]",
  "receiver_phone": "[receiver's phone number]",
  "receiver_address": "[detail address (number, street)]",
  "receiver_location_id": [delivery location id],

  "size_lenght": [parcel's length],
  "size_width": [parcel's width],
  "size_height": [parcel's height],
  "weight": [parcel's weight],

  "service_id": [exsited delivery service id],
}
```
    - _Optional_

```json
{
  "type": "[parcel's type]",
  "handle_instruction": "[order's note]",
  "expected_pickup_date": "[date time]",
  "expected_pickup_session": [0 | 1 | 2 | 3],
  "expected_delivery_date": "[date time]",
  "expected_delivery_session": [0 | 1 | 2 | 3],

  "coupon_code": "[coupon code]",
  "customer_order_code": "[customer order's code]",
  "fee_payer": [0 (default - shop) | 1 (shop's customer)],
  "cod": [cod amount],
  "return_method": [0 | 1 (default)],
  "value": [0 (default) | 1],
}
```

**Data example**

```json
{
  "sender_name": "Customer",
  "sender_phone": "0123456789",
  "sender_address": "115 Phùng Văn Cung, F2, Phường 2",
  "sender_location_id": 1,
  "sender_longitude": 106.6823217,
  "sender_latitude": 10.8021149,
  
  "receiver_name": "Bắp Cải",
  "receiver_phone": "0906663441",
  "receiver_address": "499/1L Đường Mã Lò P.Bình Hưng Hòa",
  "receiver_location_id": 9,
  "receiver_longitude": 106.59968,
  "receiver_latitude": 10.7726098,
  
  "customer_order_code": "123ABC",
  "type": "Quần Áo",
  "size_lenght": 10,
  "size_width": 10,
  "size_height": 5,
  "weight": 500,
  "value": 185000,
  "cod": 200000,
  "handle_instruction": "Không cho thử",
  "expected_pickup_date": "16/7/2018",
  "expected_pickup_session": 0,
  "expected_delivery_date": "16/7/2018",
  "expected_delivery_session": 0,
  
  "service_id": 1,
  "coupon_code": "",
  "fee_payer": 0
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "sender_name": "Customer",
        "sender_phone": "0123456789",
        "sender_address": "115 Phùng Văn Cung, F2, Phường 2",
        "sender_location_id": 1,
        "sender_longitude": 106.6823217,
        "sender_latitude": 10.8021149,
        "receiver_name": "Bắp Cải",
        "receiver_phone": "0906663441",
        "receiver_address": "499/1L Đường Mã Lò P.Bình Hưng Hòa",
        "receiver_location_id": 9,
        "receiver_longitude": 106.59968,
        "receiver_latitude": 10.7726098,
        "customer_order_code": "123ABC",
        "type": "Quần Áo",
        "size_lenght": 10,
        "size_width": 10,
        "size_height": 5,
        "weight": 500,
        "value": 185000,
        "cod": 200000,
        "handle_instruction": "Không cho thử",
        "service_id": 1,
        "coupon_code": "",
        "fee_payer": 0,
        "user_id": 5,
        "owner_id": 5,
        "return_method": 1,
        "fee_paid": 0,
        "prepaid": 0,
        "route_text": "Custom - [LH]Q1.Q1.[GH]BTan",
        "order_code": "O1531726321",
        "order_status_id": 1,
        "insurance_fee": 0,
        "delivery_fee": 19000,
        "cash": 219000,
        "return_money": 181000,
        "created": "2018-07-16T14:32:01",
        "modified": "2018-07-16T14:32:01",
        "id": 116
    },
    "paging": [],
    "message": "Created order"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `409 CONFLICT`

**Content** :

```json
{
    "success": false,
    "data": {
        "sender_name": "Empty"
    },
    "paging": [],
    "message": "Required input invalid"
}
```

```json
{
    "success": false,
    "data": {
        "Lenght limit": 100
    },
    "paging": [],
    "message": "Over length limit"
}
```