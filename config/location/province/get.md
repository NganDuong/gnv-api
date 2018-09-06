# Config Management: PROVINCE LOCATION - GET

Use to get location infomation.

**URL** : `/configs/locations/provinces/[id]`

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
            "name": "Hà Nội",
            "mining_text": "HN",
            "group_location_id": 0,
            "created": "2018-06-28T10:00:00+07:00",
            "modified": "2018-06-28T10:00:00+07:00",
            "group_location": null,
            "districts": [
                {
                    "id": 6,
                    "name": "Ba Đình",
                    "mining_text": "BĐ",
                    "province_id": 2,
                    "created": "2018-05-09T00:11:13+07:00",
                    "modified": "2018-05-09T00:11:13+07:00",
                    "location_id": 4
                },
                {
                    "id": 7,
                    "name": "Hoàn Kiếm",
                    "mining_text": "HK",
                    "province_id": 2,
                    "created": "2018-05-09T00:11:24+07:00",
                    "modified": "2018-05-09T00:11:24+07:00",
                    "location_id": null
                },
                {
                    "id": 8,
                    "name": "Hai Bà Trưng",
                    "mining_text": "HBT",
                    "province_id": 2,
                    "created": "2018-05-09T00:11:35+07:00",
                    "modified": "2018-05-09T00:11:35+07:00",
                    "location_id": null
                },
                {
                    "id": 9,
                    "name": "Đống Đa",
                    "mining_text": "ĐĐ",
                    "province_id": 2,
                    "created": "2018-05-09T00:11:58+07:00",
                    "modified": "2018-05-09T00:11:58+07:00",
                    "location_id": null
                }
            ]
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found province(s)"
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
    "message": "province not found"
}
```