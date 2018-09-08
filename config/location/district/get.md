# Config Management: DISTRICT LOCATION - GET

Use to get district infomation.

**URL** : `/configs/locations/districts/[id]`

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
            "name": "Quận 1",
            "mining_text": "Q1",
            "province_id": 1,
            "created": "2018-05-09T07:09:38",
            "modified": "2018-05-09T07:09:38",
            "location": {
                "id": 1,
                "support_type_id": 3,
                "location_type_id": 1,
                "district_id": 1,
                "province_id": 1,
                "created": "2018-05-09T07:18:12",
                "modified": "2018-05-09T07:18:12"
            },
            "province": {
                "id": 1,
                "name": "Hồ Chí Minh",
                "mining_text": "HCM",
                "group_location_id": 0,
                "created": "2018-06-28T17:00:00",
                "modified": "2018-06-28T17:00:00"
            }
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found district(s)"
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
    "message": "district not found"
}
```