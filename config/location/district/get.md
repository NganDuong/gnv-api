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
        },
        {
            "id": 2,
            "name": "Quận 2",
            "mining_text": "Q2",
            "province_id": 1,
            "created": "2018-05-09T07:10:02",
            "modified": "2018-05-09T07:10:02",
            "location": {
                "id": 8,
                "support_type_id": 3,
                "location_type_id": 1,
                "district_id": 2,
                "province_id": 1,
                "created": "2018-06-14T11:13:57",
                "modified": "2018-06-14T11:13:57"
            },
            "province": {
                "id": 1,
                "name": "Hồ Chí Minh",
                "mining_text": "HCM",
                "group_location_id": 0,
                "created": "2018-06-28T17:00:00",
                "modified": "2018-06-28T17:00:00"
            }
        },
        {
            "id": 3,
            "name": "Quận 3",
            "mining_text": "Q3",
            "province_id": 1,
            "created": "2018-05-09T07:10:08",
            "modified": "2018-05-09T07:10:08",
            "location": {
                "id": 7,
                "support_type_id": 3,
                "location_type_id": 1,
                "district_id": 3,
                "province_id": 1,
                "created": "2018-06-14T11:13:51",
                "modified": "2018-06-14T11:13:51"
            },
            "province": {
                "id": 1,
                "name": "Hồ Chí Minh",
                "mining_text": "HCM",
                "group_location_id": 0,
                "created": "2018-06-28T17:00:00",
                "modified": "2018-06-28T17:00:00"
            }
        },
        {
            "id": 4,
            "name": "Quận 4",
            "mining_text": "Q4",
            "province_id": 1,
            "created": "2018-05-09T07:10:14",
            "modified": "2018-05-09T07:10:14",
            "location": {
                "id": 6,
                "support_type_id": 3,
                "location_type_id": 1,
                "district_id": 4,
                "province_id": 1,
                "created": "2018-06-14T11:13:45",
                "modified": "2018-06-14T11:13:45"
            },
            "province": {
                "id": 1,
                "name": "Hồ Chí Minh",
                "mining_text": "HCM",
                "group_location_id": 0,
                "created": "2018-06-28T17:00:00",
                "modified": "2018-06-28T17:00:00"
            }
        },
        {
            "id": 5,
            "name": "Quận 5",
            "mining_text": "Q5",
            "province_id": 1,
            "created": "2018-05-09T07:10:18",
            "modified": "2018-05-09T07:10:18",
            "location": {
                "id": 5,
                "support_type_id": 3,
                "location_type_id": 1,
                "district_id": 5,
                "province_id": 1,
                "created": "2018-06-14T11:13:30",
                "modified": "2018-06-14T11:13:30"
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
        "next": "/configs/locations/districts?page=2",
        "total": 16,
        "total_page": 4
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