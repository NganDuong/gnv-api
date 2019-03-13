# Announcements Management: GET

Use to delete a announcement.

**URL** : `/announcements/[id]`

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
            "id": 7,
            "public_date": "2018-11-07T11:34:24+07:00",
            "expire_date": "2018-11-11T00:00:00+07:00",
            "highlight": 0,
            "status": 1,
            "user_group_id": 0,
            "created": "2018-11-07T10:39:37+07:00",
            "modified": "2018-11-07T11:34:24+07:00",
            "contents": [
                {
                    "id": 1,
                    "announcement_id": 7,
                    "content_type": 1,
                    "content": "NEW BRAND",
                    "created": "2018-11-07T10:39:37+07:00",
                    "modified": "2018-11-07T10:39:37+07:00"
                },
                {
                    "id": 2,
                    "announcement_id": 7,
                    "content_type": 2,
                    "content": "new opening @ 07/11/2018",
                    "created": "2018-11-07T10:39:37+07:00",
                    "modified": "2018-11-07T10:39:37+07:00"
                },
                {
                    "id": 3,
                    "announcement_id": 7,
                    "content_type": 3,
                    "content": "Discount 10% for 10 orders",
                    "created": "2018-11-07T10:39:37+07:00",
                    "modified": "2018-11-07T10:39:37+07:00"
                }
            ],
            "banner": {
                "id": 7,
                "target_id": 7,
                "target_type": "Announcements",
                "field": "Banner",
                "path": "/uploads/files/banners/images.jpeg",
                "created": "2018-11-07T10:39:37+07:00",
                "modified": "2018-11-07T10:39:37+07:00"
            }
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Tìm thấy announcement(s)"
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
    "message": "announcement not found"
}
```