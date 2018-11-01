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
    "data": [],
    "paging": [],
    "message": "Can use this coupon"
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