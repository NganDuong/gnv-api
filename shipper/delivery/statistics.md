# Shipper: GET DELIVERY STATISTICS

Use to get shipper's current DRS statistics.

**URL** : `/orders/delivery/statistics`

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
        "delivered": 0,
        "delivering": 0,
        "failed": 0,
        "total": 0
    },
    "paging": [],
    "message": "Calculated"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```