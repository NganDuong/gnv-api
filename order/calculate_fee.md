# Order Management: CALCULATE FEE

Use to calculate order's fee.

**URL** : `/orders/fees`

**Method** : `GET`

**Content-Type** : application/json

**Auth required** : YES

**URL query params**

```json
{
    "weight": [parcel's weight],
    "length": [parcel's length],
    "width": [parcel's width],
    "height": [parcel's height],
    "service_id": [exsited delivery service id],
    "cod": [cod amount],
    "coupon_code": "[coupon code]",
    "value": [parcel's value],
}
```

**URL example**

/orders/fees?weight=10000&length=100&width=100&height=100&service_id=100&cod=1&service_id=1&value=100000

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "service_fee": 61000,
        "cod_fee": 10000,
        "insurance_fee": 50000,
        "total": 121000
    },
    "paging": [],
    "message": "Fees calculated"
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
        "Height limit": 100
    },
    "paging": [],
    "message": "Over height limit"
}
```