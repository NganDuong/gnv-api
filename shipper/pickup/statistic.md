# Shipper: GET PICKUP STATISTICS

Use to get shipper's current PRS statistics.

**URL** : `/orders/pickup/statistics`

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
        "picked": 0,
        "picking": 1,
        "failed": 0,
        "total": 1
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