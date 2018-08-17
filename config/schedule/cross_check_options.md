# Config Management: CROSS-CHECK SCHEDULE'S OPTIONS - GET

Use to get cross-check schedule's options.

**URL** : `/configs/schedules/options/{type}`

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
            "date": 1,
            "description": "Monday"
        },
        {
            "id": 2,
            "date": 2,
            "description": "Tuesday"
        },
        {
            "id": 3,
            "date": 3,
            "description": "Wednesday"
        },
        {
            "id": 4,
            "date": 4,
            "description": "Thursday"
        },
        {
            "id": 5,
            "date": 5,
            "description": "Friday"
        },
        {
            "id": 6,
            "date": 6,
            "description": "Saturday"
        },
        {
            "id": 7,
            "date": 7,
            "description": "Sunday"
        }
    ],
    "paging": {
        "total": 7
    },
    "message": "Found options"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
```