# User Management: REGISTER PUSH NOTIFICATION

Use to register a firebase push notification token.

**URL** : `/users/notifications/register`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
    "device_token": "[firebase token]",
    "device_type": [1 | 2 | 3],
}
```
    -_Note_:
        - If device type is web: ```device_type``` is 1.
        - If device type is android: ```device_type``` is 2.
        - If device type is iOS: ```device_type``` is 3.

**Data example**

```json
{
    "device_token": "fuCvW2jv10A:APA91bHXOCynyuHHca-7PRM_x6YyG2FGTN2R5oaGCKLCBnSzv5GwWiAXjCU8RqC27Ahi7azYOJBZzMKIu0NYUZKZ3Y_RsMJ1Rr6qQq5PZtZvwEVocnca1BY7hODAA2Pd0XAT7alNEyfm",
    "device_type": 1
}
```

## Success Response

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 1,
        "user_id": "1",
        "device_token": "fuCvW2jv10A:APA91bHXOCynyuHHca-7PRM_x6YyG2FGTN2R5oaGCKLCBnSzv5GwWiAXjCU8RqC27Ahi7azYOJBZzMKIu0NYUZKZ3Y_RsMJ1Rr6qQq5PZtZvwEVocnca1BY7hODAA2Pd0XAT7alNEyfm",
        "created": "2018-06-08T06:55:06+00:00",
        "modified": "2018-06-08T06:55:24+00:00",
        "device_type": 1
    },
    "paging": [],
    "message": "Registered userdevicetoken"
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
        "push_destination": "Empty"
    },
    "paging": [],
    "message": "Required input invalid"
}
```