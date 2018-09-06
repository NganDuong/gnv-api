# Config Management: SUPPORT BANK - GET

Use to get a bank.

**URL** : `/configs/banks/{id}`

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
            "name": "Ngân hàng Chính sách xã hội",
            "short_name": "NHCSXH/VBSP",
            "swift_code": "",
            "created": "2018-07-19T13:25:41+07:00",
            "modified": "2018-07-19T13:25:41+07:00"
        },
        {
            "id": 2,
            "name": "Ngân hàng Phát triển Việt Nam",
            "short_name": "VDB",
            "swift_code": "",
            "created": "2018-07-19T13:26:07+07:00",
            "modified": "2018-07-19T13:26:07+07:00"
        },
        {
            "id": 3,
            "name": "Ngân hàng Xây dựng",
            "short_name": "CB",
            "swift_code": "",
            "created": "2018-07-19T13:26:41+07:00",
            "modified": "2018-07-19T13:26:41+07:00"
        },
        {
            "id": 4,
            "name": "Ngân hàng Đại Dương",
            "short_name": "Oceanbank",
            "swift_code": "",
            "created": "2018-07-19T13:26:59+07:00",
            "modified": "2018-07-19T13:26:59+07:00"
        },
        {
            "id": 5,
            "name": "Ngân hàng Dầu Khí Toàn Cầu",
            "short_name": "GPBank",
            "swift_code": "",
            "created": "2018-07-19T13:27:20+07:00",
            "modified": "2018-07-19T13:27:20+07:00"
        }
    ],
    "paging": {
        "next": "/configs/banks/?page=2",
        "total": 6
    },
    "message": "Found supportbank(s)"
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
    "message": "supportbank not found"
}
```