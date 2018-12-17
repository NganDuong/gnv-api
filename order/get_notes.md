# Order Management: GET NOTES

Use to get order's notes infomation.

**URL** : `/orders/notes/{id}`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "order_id": [existed order id],
    "user_id": [existed user id],
    "order_note_reason_id": [exsited note reason id],
    "field": "[Shop | ...]",
    "description": "[content]",
    "note_date": "[datetime]",
    "created": "[datetime]",
}
```

**URL example**

/orders?order_id=1

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": [
        {
            "id": 46,
            "user_id": 0,
            "order_id": 16,
            "order_note_reason_id": 0,
            "field": "Đã nhận",
            "description": "Tuyến giao hàng: Custom - [LH]Q10.HubQuan11.[GH]TPh",
            "note": "",
            "note_date": null,
            "created": "2018-12-14T15:49:47",
            "modified": "2018-12-14T15:49:47",
            "user": null,
            "order_note_reason": null
        },
        {
            "id": 55,
            "user_id": 1,
            "order_id": 16,
            "order_note_reason_id": 0,
            "field": "Đã duyệt",
            "description": "Duyệt bởi DDD_global_admin",
            "note": "",
            "note_date": null,
            "created": "2018-12-14T15:50:07",
            "modified": "2018-12-14T15:50:07",
            "user": {
                "username": "DDD_global_admin"
            },
            "order_note_reason": null
        },
        {
            "id": 58,
            "user_id": 3,
            "order_id": 16,
            "order_note_reason_id": 0,
            "field": "Chuẩn bị lấy",
            "description": "Chuẩn bị lấy hàng từ: 14/12/2018 - Ca chiều",
            "note": "",
            "note_date": null,
            "created": "2018-12-14T15:50:24",
            "modified": "2018-12-14T15:50:24",
            "user": {
                "username": "Zakhun"
            },
            "order_note_reason": null
        },
        {
            "id": 65,
            "user_id": 44,
            "order_id": 16,
            "order_note_reason_id": 0,
            "field": "Đã Lấy",
            "description": "Đơn hàng được lấy bởi DingDongShipper",
            "note": "",
            "note_date": null,
            "created": "2018-12-14T15:51:42",
            "modified": "2018-12-14T15:51:42",
            "user": {
                "username": "DingDongShipper"
            },
            "order_note_reason": null
        },
        {
            "id": 71,
            "user_id": 1,
            "order_id": 16,
            "order_note_reason_id": 0,
            "field": "Đang ở kho",
            "description": "Đã nhập kho: HubQuan11.WB1544777583",
            "note": "",
            "note_date": null,
            "created": "2018-12-14T15:53:03",
            "modified": "2018-12-14T15:53:03",
            "user": {
                "username": "DDD_global_admin"
            },
            "order_note_reason": null
        }
    ],
    "paging": {
        "total": 5,
        "total_page": 1
    },
    "message": "Tìm thấy ordernote(s)"
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
    "message": "ordernote not found"
}
```