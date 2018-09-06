# Config Management: LOCATION TYPE - GET

Use to get location's type infomation.

**URL** : `/configs/locations/types/{id}`

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
            "name": "Nội thành",
            "created": "2018-06-27T10:12:56+07:00",
            "modified": "2018-06-27T10:12:56+07:00"
        },
        {
            "id": 2,
            "name": "Ngoại thành",
            "created": "2018-06-27T10:14:47+07:00",
            "modified": "2018-06-27T10:14:47+07:00"
        },
        {
            "id": 3,
            "name": "Ngoại thành 2",
            "created": "2018-06-27T10:15:39+07:00",
            "modified": "2018-06-27T10:15:39+07:00"
        }
    ],
    "paging": {
        "total": 3
    },
    "message": "Found locationtype(s)"
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
    "message": "locationtype not found"
}
```