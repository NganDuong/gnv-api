# Order Management: GET

Use to get user's order infomation.

**URL** : `/orders/guests?order_code={string}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : NO

**Data params**

**Data example**

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "summary": {
            "order_code": "P1540400208",
            "current_location": "Q12.WB1540400704",
            "sender_name": "Chi Nhánh 01",
            "sender_phone": "098766789",
            "sender_address": "109Bis Phạm Ngũ Lão, Quận 1, Hồ Chí Minh, Việt Nam",
            "sender_location_id": 1,
            "sender_longitude": 106.695736,
            "sender_latitude": 10.769455,
            "receiver_name": "Ngan",
            "receiver_phone": "0123123123",
            "receiver_address": "1234 Quốc lộ 1A, Thới An, Quận 12, Hồ Chí Minh, Việt Nam",
            "receiver_location_id": 12,
            "receiver_longitude": 106.660165,
            "receiver_latitude": 10.862245,
            "shipper_id": null,
            "fee_payer": 0,
            "fee_paid": 1,
            "order_status_id": 6,
            "size_lenght": 100,
            "size_width": 100,
            "size_height": 100,
            "weight": 10000,
            "cod": 150000,
            "pickup_date": "2018-10-25T00:00:00+07:00",
            "delivery_date": null,
            "return_date": null,
            "service": {
                "id": 2,
                "name": "Tiêu Chuẩn",
                "group_location_type_id": 1,
                "location_type_id": 2,
                "description": "",
                "created_before": "2018-10-25T23:10:00+07:00",
                "delivery_day": 1,
                "delivery_before": "2018-10-25T23:10:00+07:00",
                "standard_weight": 3000,
                "price": 29000,
                "extra_weight": 500,
                "extra_weight_price": 3000,
                "created": "2018-10-10T23:57:42+07:00",
                "modified": "2018-10-10T23:57:42+07:00"
            },
            "shipper": null,
            "order_status": {
                "id": 6,
                "name": "Scanned/Checked",
                "customer_display": "Scanned/Checked",
                "color": "#50E3C2",
                "created": "2018-05-07T06:00:00+07:00",
                "modified": "2018-05-22T22:46:24+07:00"
            },
            "sender": "Name: Chi Nhánh 01 - Phone: 098766789 - Address: 109Bis Phạm Ngũ Lão, Quận 1, Hồ Chí Minh, Việt Nam, Quận 1, Hồ Chí Minh",
            "receiver": "Name: Ngan - Phone: 0123123123 - Address: 1234 Quốc lộ 1A, Thới An, Quận 12, Hồ Chí Minh, Việt Nam, Quận 12, Hồ Chí Minh",
            "size": "100x100x100",
            "sender_address_district": "Quận 1",
            "sender_address_province": "Hồ Chí Minh",
            "receiver_address_district": "Quận 12",
            "receiver_address_province": "Hồ Chí Minh",
            "insurance_fee": 0,
            "delivery_fee": 71000,
            "return_money": 221000,
            "cash": 150000,
            "pickup_session": "morning",
            "expected_pickup_date": "2018-10-25T00:00:00+07:00",
            "expected_pickup_session": "morning",
            "expected_delivery_date": "2018-10-25T00:00:00+07:00",
            "expected_delivery_session": "morning"
        },
        "details": [
            {
                "id": 12,
                "user_id": 0,
                "order_id": 3,
                "order_note_reason_id": 0,
                "field": "Order Received",
                "description": "Route: Quan11-Quan12 - [LH]Q1.Q11.Q12.[GH]Q12",
                "note": "",
                "note_date": null,
                "created": "2018-10-24T23:56:48+07:00",
                "modified": "2018-10-24T23:56:48+07:00"
            },
            {
                "id": 14,
                "user_id": 1,
                "order_id": 3,
                "order_note_reason_id": 0,
                "field": "Order Approved",
                "description": "Approved by admin",
                "note": "",
                "note_date": null,
                "created": "2018-10-24T23:57:59+07:00",
                "modified": "2018-10-24T23:57:59+07:00"
            },
            {
                "id": 16,
                "user_id": 5,
                "order_id": 3,
                "order_note_reason_id": 0,
                "field": "To Be Picked Up",
                "description": "Ready to be picked up from: 10/25/18, 12:00 AM to 10/25/18, 11:59 AM",
                "note": "",
                "note_date": null,
                "created": "2018-10-24T23:58:09+07:00",
                "modified": "2018-10-24T23:58:09+07:00"
            },
            {
                "id": 18,
                "user_id": 3,
                "order_id": 3,
                "order_note_reason_id": 0,
                "field": "Picked Up",
                "description": "Order is picked by shipper",
                "note": "",
                "note_date": null,
                "created": "2018-10-25T00:00:51+07:00",
                "modified": "2018-10-25T00:00:51+07:00"
            },
            {
                "id": 20,
                "user_id": 1,
                "order_id": 3,
                "order_note_reason_id": 0,
                "field": "Scanned/Checked",
                "description": "Arrival at PO: Q11.WB1540400472",
                "note": "",
                "note_date": null,
                "created": "2018-10-25T00:01:12+07:00",
                "modified": "2018-10-25T00:01:12+07:00"
            }
        ]
    },
    "paging": {
        "next": "/orders/guests?order_code=P1540400208&page=2",
        "total": 8,
        "total_page": 2
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