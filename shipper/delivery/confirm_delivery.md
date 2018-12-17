# Shipper: CONFIRM DELIVERED UP AN ORDER

Use to confirm picked up an order.

**URL** : `/orders/deliver/confirm/{id}`

**Method** : `PATCH`

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
    "data": "P1544777369",
    "paging": [],
    "message": "Xác nhận đã giao hàng"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```