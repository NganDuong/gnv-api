# Shipper: CONFIRM PICKED UP AN ORDER

Use to confirm picked up an order.

**URL** : `/orders/pickup/confirm/{id}`

**Method** : `PATCH`

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
        "id": 2,
        "order_code": "O1528042565",
        "customer_order_code": "12312312",
        "owner_id": 2,
        "warehouse_id": 0,
        "pdrs_id": 9,
        "route_id": 0,
        "route_text": "Custom - [LH]BĐ.HN.Q1.[GH]Q1",
        "last_location": "",
        "current_location": "",
        "sender_name": "A",
        "sender_phone": "0123456789",
        "sender_address": "104 NCT",
        "sender_location_id": 4,
        "sender_longitude": 0,
        "sender_latitude": 0,
        "receiver_name": "B",
        "receiver_phone": "0123456789",
        "receiver_address": "104 NCT",
        "receiver_location_id": 1,
        "receiver_longitude": 0,
        "receiver_latitude": 0,
        "shipper_id": 3,
        "service_id": 1,
        "fee_payer": 0,
        "fee_paid": 1,
        "order_status_id": 5,
        "handle_instruction": "Note",
        "coupon_code": "",
        "type": "ABC",
        "size_lenght": 10,
        "size_width": 10,
        "size_height": 10,
        "weight": 10,
        "value": 50000,
        "cod": 6000,
        "prepaid": 34000,
        "return_method": 1,
        "pickup_date": "2018-06-03T17:54:46+00:00",
        "delivery_date": null,
        "return_date": null,
        "expected_pickup_from": "2018-05-31T00:00:00+00:00",
        "expected_pickup_to": "2018-05-31T00:00:00+00:00",
        "expected_delivery_from": "2019-01-02T00:00:00+00:00",
        "expected_delivery_to": "2019-01-02T00:00:00+00:00",
        "pickup_times": 3,
        "delivery_times": 0,
        "return_times": 0,
        "created": "2018-06-03T16:16:05+00:00",
        "modified": "2018-06-03T17:54:46+00:00"
    },
    "paging": [],
    "message": "Confirm picked"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```