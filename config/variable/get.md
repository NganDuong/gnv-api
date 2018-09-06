# Config Management: VARIABLES - GET

Use to get variable(s).

**URL** : `/configs/variables/{id}`

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
            "id": 1,
            "name": "PARCEL_WEIGHT_LIMIT",
            "value": 15000,
            "type": 0,
            "description": "Description"
        },
        {
            "id": 2,
            "name": "PARCEL_SURCHARGE",
            "value": 5000,
            "type": 0,
            "description": "Description"
        },
        {
            "id": 3,
            "name": "PARCEL_WEIGHT_SURCHARGE",
            "value": 5,
            "type": 0,
            "description": "Description"
        },
        {
            "id": 4,
            "name": "PARCEL_SIZE_FEE",
            "value": 0,
            "type": 1,
            "description": "Description"
        },
        {
            "id": 5,
            "name": "PARCEL_SIZE_CONVERT",
            "value": 6000,
            "type": 0,
            "description": "Description"
        }
    ],
    "paging": {
        "next": "/configs/variables?page=2",
        "total": 19,
        "total_page": 4
    },
    "message": "Found configvariable(s)"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "configvariable(s) not found"
}
```