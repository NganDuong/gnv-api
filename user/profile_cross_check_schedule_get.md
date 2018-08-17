# User Management: PROFILE - CROSS-CHECK SCHEDULE - GET

Use to get user's cross-check schedule.

**URL** : `/users/profile/schedules/crossCheck`

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
            "user_id": 5,
            "cross_check_schedule_id": 1,
            "created": "2018-06-21T10:43:44+07:00",
            "modified": "2018-06-21T10:43:44+07:00",
            "cross_check_schedule": {
                "id": 1,
                "type": 1,
                "name": "Đối soát theo tháng",
                "created": "2018-06-20T17:00:07+07:00",
                "modified": "2018-06-21T10:00:52+07:00"
            }
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found usercrosscheckschedule(s)"
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
    "message": "usercrosscheckschedule not found"
}
```