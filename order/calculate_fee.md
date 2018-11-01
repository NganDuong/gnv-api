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
    "source_location_id": [source_location_id],
    "dest_location_id": [dest_location_id],
}
```

**URL example**

/orders/fees?weight=3500&length=20&width=&source_location_id=1&dest_location_id=7&service_id=2&cod=350000&value=350000

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "0": {
            "name": "Service",
            "amount": 20000
        },
        "service_fee": 20000,
        "before_discount": 20000,
        "discount": 15000,
        "total": 5000
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