# Config Management: COUPON - CHECK

Use to get coupons.

**URL** : `/configs/orders/coupons/check?code={coupon_code}&user_id={user_id}`

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
    "data": {
        "id": 1,
        "code": "GNV123",
        "is_percent": 1,
        "rate": 0.5,
        "use_times": 0,
        "used_times": 1,
        "from_date": "2018-07-01T00:00:00+07:00",
        "to_date": "2018-07-10T00:00:00+07:00",
        "max_use_per_user": 1,
        "created": "2018-07-03T14:53:07+07:00",
        "modified": "2018-07-03T15:15:16+07:00"
    },
    "paging": [],
    "message": "Coupon is valid"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "Unable to use this coupon"
}
```