# Order Management: REQUEST CREATE

Use to create a request for existed order.

**URL** : `/orders/requests`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
  "order_id": [existed order id],
  "order_request_type_id": [existed order request type id],
  "description": "[content]"
}
```

**Data example**

```json
{
  "order_id": 1,
  "order_request_type_id": 1,
  "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA"
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "order_id": 1,
        "order_request_type_id": 1,
        "description": "Cập nhật tên người gửi thành  AAAAAAAAAAA",
        "user_id": 1,
        "creater_id": 1,
        "created": "2018-05-21T08:01:55+00:00",
        "modified": "2018-05-21T08:01:55+00:00",
        "id": 1
    },
    "paging": [],
    "message": "Created orderrequest"
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
        "order_request_type_id": {
            "_existsIn": "Invalid request type id"
        }
    },
    "paging": [],
    "message": "Unable to create orderrequest"
}
```