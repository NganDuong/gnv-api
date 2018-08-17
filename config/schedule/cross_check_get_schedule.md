# Config Management: CROSS-CHECK SCHEDULE - GET

Use to get cross-check schedule.

**URL** : `/configs/schedules/crossCheck`

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
            "type": 0,
            "name": "Đối soát theo tuần",
            "created": "2018-06-20T17:00:07+07:00",
            "modified": "2018-06-20T17:00:07+07:00",
            "cross_check_schedule_details": [
                {
                    "id": 1,
                    "cross_check_schedule_id": 1,
                    "cross_check_schedule_option_id": 1,
                    "created": "2018-06-20T17:00:07+07:00",
                    "modified": "2018-06-20T17:00:07+07:00",
                    "cross_check_schedule_option": {
                        "date": 1,
                        "description": "Monday"
                    }
                },
                {
                    "id": 2,
                    "cross_check_schedule_id": 1,
                    "cross_check_schedule_option_id": 2,
                    "created": "2018-06-20T17:00:07+07:00",
                    "modified": "2018-06-20T17:00:07+07:00",
                    "cross_check_schedule_option": {
                        "date": 2,
                        "description": "Tuesday"
                    }
                }
            ]
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found schedules"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
```