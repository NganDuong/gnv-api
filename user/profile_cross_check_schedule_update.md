# User Management: PROFILE - CROSS-CHECK SCHEDULE - UPDATE

Use to create/update user's cross-check schedule.

**URL** : `/users/profile/schedules/crossCheck/{id}`

**Method** : `PUT`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
    "cross_check_schedule_id": [existed cross_check_schedule_id]
}
```

**Data example**

```json
{
    "cross_check_schedule_id": 1
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
        "user_id": 5,
        "cross_check_schedule_id": 1,
        "created": "2018-06-21T10:43:44+07:00",
        "modified": "2018-06-21T10:43:44+07:00"
    },
    "paging": [],
    "message": "Saved schedule"
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
            "_isUnique": "This user_id has already been used."
        }
    },
    "paging": [],
    "message": "Unable to saved schedule"
}
```