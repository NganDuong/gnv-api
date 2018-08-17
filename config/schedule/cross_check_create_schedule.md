# Config Management: CROSS-CHECK SCHEDULE - CREATE

Use to create a cross-check schedule.

**URL** : `/configs/schedules/crossCheck`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    _Required_

```json
{
  "type": [0 | 1],
  "name": "[name of this schedule]",
  "option_ids": [array of schedule's option id]
}
```

**Data example**

```json
{
  "type": 1,
  "name": "Đối soát theo tháng",
  "option_ids": [1,2]
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "type": 1,
        "name": "Đối soát theo tháng",
        "option_ids": [
            1,
            2
        ],
        "created": "2018-06-20T17:02:14+07:00",
        "modified": "2018-06-20T17:02:14+07:00",
        "id": 2
    },
    "paging": [],
    "message": "Created"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "success": false,
    "data": {
        "name": {
            "unique": "The provided value is invalid"
        }
    },
    "paging": [],
    "message": "Invalid input"
}
```