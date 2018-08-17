# User Management: PROFILE - STORE - CREATE

Use to create user's store infomation.

**URL** : `/users/profile/stores`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
  "name": "[contact name]",
  "phone": "[contact phone number]",
  "address": "[detail address (number, street)]",
  "location_id": [exsited location_id],
  "longitude": [longitude],
  "latitude": [latitude]
}
```

    - _Optional_

```json
{
  "default_store": [0 (default) | 1],
}
```

**Data example**

```json
{
   "name": "Duong Thi Kim Ngan",
  "phone": "0123456789",
  "address": "105 NCT",
  "location_id": 2,
  "longitude": 1.232323,
  "latitude": 1.232323
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "name": "Duong Thi Kim Ngan",
        "phone": "0123456789",
        "address": "105 NCT",
        "location_id": 2,
        "longitude": 1.232323,
        "latitude": 1.232323,
        "user_id": 1,
        "default_store": 1,
        "created": "2018-06-11T03:39:15+00:00",
        "modified": "2018-06-11T03:39:15+00:00",
        "id": 2
    },
    "paging": [],
    "message": "Created store"
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
        "user_id": {
            "_isUnique": "This user_id, location_id, name & phone combination has already been used."
        }
    },
    "paging": [],
    "message": "Unable to create store"
}
```