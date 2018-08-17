# User Management: PROFILE - STORE - UPDATE

Use to create user's store infomation.

**URL** : `/users/profile/stores/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Optional_

```json
{
  "name": "[contact name]",
  "phone": "[contact phone number]",
  "address": "[detail address (number, street)]",
  "location_id": [exsited location_id]
}
```

**Data example**

```json
{
  "default_store": 0
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 1,
        "user_id": 2,
        "location_id": 1,
        "name": "Duong Thi Kim Ngan",
        "phone": "0123456789",
        "address": "105 NCT",
        "default_store": 1,
        "created": "2018-05-10T18:03:51+00:00",
        "modified": "2018-05-10T18:03:51+00:00"
    },
    "paging": [],
    "message": "Updated store"
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
    "message": "Unable to update store"
}
```

Or

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "store not found"
}
```