# User Management: PROFILE - STORE - GET

Use to get user's store infomation.

**URL** : `/users/profile/stores/{id}`

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
            "id": 2,
            "user_id": 1,
            "location_id": 2,
            "longitude": 1.232323,
            "latitude": 1.232323,
            "name": "Duong Thi Kim Ngan",
            "phone": "0123456789",
            "address": "105 NCT",
            "default_store": 1,
            "created": "2018-06-11T03:39:15+00:00",
            "modified": "2018-06-11T03:39:15+00:00",
            "location": {
                "id": 2,
                "support_type_id": 2,
                "area_type_id": 1,
                "district_id": 2,
                "province_id": 1,
                "created": "2018-05-09T07:18:57+00:00",
                "modified": "2018-05-09T07:18:57+00:00",
                "district": {
                    "id": 2,
                    "name": "Quận 2",
                    "mining_text": "Q2",
                    "province_id": 1,
                    "created": "2018-05-09T07:10:02+00:00",
                    "modified": "2018-05-09T07:10:02+00:00"
                },
                "province": {
                    "id": 1,
                    "name": "Hồ Chí Minh",
                    "mining_text": "HCM",
                    "created": "2018-05-09T07:08:18+00:00",
                    "modified": "2018-05-09T07:08:18+00:00"
                }
            }
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found store(s)"
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
    "message": "store not found"
}
```