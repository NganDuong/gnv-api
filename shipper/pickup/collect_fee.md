# Shipper: CONFIRM COLLECTED FEE ON PICKUP ORDERS

Use to confirm collected fees on pickup orders.

**URL** : `/orders/pickup/collectFees/{id}`

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
    "data": 34000,
    "paging": [],
    "message": "Collected fee from sender"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```