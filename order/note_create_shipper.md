# Order Management: CREATE CALL LOG

Use to create a call log for an existed order.

**URL** : `/orders/notes`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
  "order_id": [existed order id],
  "description": "[content]"
}
```

**Data example**

```json
{
  "order_id": 14,
  "description": "gọi lỡ 012899400280902834057 lúc 18/09 14:22:51, chuông 7s"
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "user_id": 3,
        "order_id": 14,
        "field": "Ready To Deliver",
        "description": "gọi lỡ 012899400280902834057 lúc 18/09 14:22:51, chuông 7s",
        "created": "2018-09-26T15:14:55+07:00",
        "modified": "2018-09-26T15:14:55+07:00",
        "id": 245
    },
    "paging": [],
    "message": "Created ordernote"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `409 CONFLICT`

**Content** :

```json
{
    "success": false,
    "data": [],
    "paging": [],
    "message": "Input invalid"
}
```