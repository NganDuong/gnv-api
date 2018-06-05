# Shipper: GET Current PRS

Use to get shipper's current PRS.

**URL** : `/orders/pickup`

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
    "data": [
        {
            "sender_name": "A",
            "sender_phone": "0123456789",
            "sender_address": "104 NCT",
            "sender_location_id": 4,
            "total": 1,
            "sender_address_detail": "104 NCT, Ba Đình, Hà Nội",
            "total_to_be_picked_up": 1
        }
    ],
    "paging": [],
    "message": "Found order(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```