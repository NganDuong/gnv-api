# Config Management: LOCATION - GET

Use to get location infomation.

**URL** : `/configs/locations/[id]`

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
            "support_type_id": 3,
            "location_type_id": 1,
            "district_id": 1,
            "province_id": 1,
            "created": "2018-05-09T00:18:12+07:00",
            "modified": "2018-05-09T00:18:12+07:00",
            "province": {
                "id": 1,
                "name": "Hồ Chí Minh",
                "mining_text": "HCM",
                "group_location_id": 0,
                "created": "2018-06-28T10:00:00+07:00",
                "modified": "2018-06-28T10:00:00+07:00"
            },
            "district": {
                "id": 1,
                "name": "Quận 1",
                "mining_text": "Q1",
                "province_id": 1,
                "created": "2018-05-09T00:09:38+07:00",
                "modified": "2018-05-09T00:09:38+07:00"
            },
            "area_type": {
                "id": 1,
                "name": "Nội Thành",
                "created": "2018-06-28T10:00:00+07:00",
                "modified": "2018-06-28T10:00:00+07:00"
            },
            "location_type": {
                "id": 1,
                "name": "Nội Thành",
                "created": "2018-06-28T10:00:00+07:00",
                "modified": "2018-06-28T10:00:00+07:00"
            },
            "support_type": {
                "id": 3,
                "name": "Lấy và Giao",
                "created": "2018-05-08T03:00:00+07:00",
                "modified": "2018-05-08T03:00:00+07:00"
            }
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found location(s)"
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
    "message": "location not found"
}
```