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
            "id": 16,
            "order_code": "P1544777387",
            "customer_order_code": "",
            "owner_id": 3,
            "user_code": "G1542281784",
            "warehouse_id": 1,
            "pdrs_id": 5,
            "route_id": 0,
            "route_text": "Custom - [LH]Q10.HubQuan11.[GH]TPh",
            "last_location": "",
            "current_location": "HubQuan11.WB1544777583",
            "sender_name": "Huyền Trang ",
            "sender_phone": "0945015815",
            "sender_address": "103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam",
            "sender_location_id": 10,
            "sender_longitude": 106.676646,
            "sender_latitude": 10.76594,
            "receiver_name": "Kim Lee",
            "receiver_phone": "0986765580",
            "receiver_address": "66 Nguyễn Hữu Tiến, Phường 15, Tân Phú, Hồ Chí Minh, Việt Nam",
            "receiver_location_id": 24,
            "receiver_longitude": 106.625849,
            "receiver_latitude": 10.81017,
            "shipper_id": null,
            "service_id": 1,
            "fee_payer": 0,
            "fee_paid": 0,
            "order_status_id": 6,
            "handle_instruction": "",
            "coupon_code": "DINGDONG",
            "discount": 0,
            "type": "",
            "size_lenght": 0,
            "size_width": 0,
            "size_height": 0,
            "weight": 150,
            "value": 0,
            "cod": 1100000,
            "prepaid": 0,
            "return_method": 1,
            "pickup_date": "2018-12-17T12:00:00",
            "delivery_date": null,
            "return_date": null,
            "expected_pickup_from": "2018-12-14T12:00:00",
            "expected_pickup_to": "2018-12-14T23:59:59",
            "expected_delivery_from": "2018-12-19T00:00:00",
            "expected_delivery_to": "2018-12-19T11:59:59",
            "pickup_times": 1,
            "delivery_times": 0,
            "return_times": 0,
            "flag": -1,
            "created": "2018-12-14T15:49:47",
            "modified": "2018-12-14T15:53:03",
            "owner_code": {
                "id": 3,
                "user_code": "G1542281784",
                "username": "Zakhun",
                "name": "Trọng Hiếu"
            },
            "shipper": null,
            "pickup_delivery_run_sheet": {
                "id": 5,
                "pdrs_code": "DRS-1544777583",
                "shipper_id": 0,
                "approver_id": 0,
                "warehouse_id": null,
                "location_id": 24,
                "pickup_delivery_date_from": "2018-12-19T00:00:00",
                "pickup_delivery_date_to": "2018-12-19T11:59:59",
                "type": 1,
                "status": 0,
                "total_order": 1,
                "created": "2018-12-14T15:53:03",
                "modified": "2018-12-14T15:53:03"
            },
            "delivery_signature_photo": null,
            "delivery_photos": [],
            "pickup_signature_photo": null,
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
            "order_status": {
                "id": 6,
                "name": "Đang ở kho",
                "customer_display": "Đang ở kho",
                "customer_id": 0,
                "color": "#FFB135",
                "created": "2018-05-06T16:00:00",
                "modified": "2018-05-22T08:46:24"
            },
            "service": {
                "id": 1,
                "name": "Nội Thành",
                "group_location_type_id": 1,
                "location_type_id": 1,
                "description": "",
                "created_before": "2018-12-17T10:11:00",
                "delivery_day": 1,
                "delivery_before": "2018-12-17T23:11:00",
                "standard_weight": 5000,
                "price": 20000,
                "extra_weight": 500,
                "extra_weight_price": 3000,
                "created": "2018-11-04T20:13:50",
                "modified": "2018-11-04T20:13:50"
            },
            "sender": "Name: Huyền Trang  - Phone: 0945015815 - Address: 103 Hồ Thị Kỷ, Phường 1, Quận 10, Hồ Chí Minh, Việt Nam, Quận 10, Hồ Chí Minh",
            "receiver": "Name: Kim Lee - Phone: 0986765580 - Address: 66 Nguyễn Hữu Tiến, Phường 15, Tân Phú, Hồ Chí Minh, Việt Nam, Quận Tân Phú, Hồ Chí Minh",
            "size": "0x0x0",
            "sender_address_district": "Quận 10",
            "sender_address_province": "Hồ Chí Minh",
            "receiver_address_district": "Quận Tân Phú",
            "receiver_address_province": "Hồ Chí Minh",
            "insurance_fee": 0,
            "cod_fee": 0,
            "return_fee": 0,
            "delivery_fee": 20000,
            "service_fee": 20000,
            "return_money": 1080000,
            "cash": 1100000,
            "expected_delivery_date": "2018-12-19T00:00:00",
            "expected_delivery_session": "sáng",
            "expected_delivery_session_name": "Ca sáng",
            "expected_delivery_session_order": 1,
            "pickup_session": "chiều",
            "pickup_session_name": "Ca chiều",
            "pickup_session_order": 2,
            "expected_pickup_date": "2018-12-14T12:00:00",
            "expected_pickup_session": "chiều",
            "expected_pickup_session_name": "Ca chiều",
            "expected_pickup_session_order": 2
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Tìm thấy order(s)"
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