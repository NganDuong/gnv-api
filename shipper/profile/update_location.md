# Shipper: Create/Update current location

Use to create/update shipper's current location.

**URL** : `/users/profile/locations`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**
    _Required_

```json
{
  "longitude": [longitude],
  "latitude": [latitude]
}
```

**Data example**

```json
{
  "longitude": 1.256489,
  "latitude": 10.2354889984
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "longitude": 1.256489,
        "latitude": 10.2354889984,
        "user_id": 2,
        "created": "2018-06-11T03:05:49+00:00",
        "modified": "2018-06-11T03:05:49+00:00",
        "id": 1
    },
    "paging": [],
    "message": "Updated location."
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```