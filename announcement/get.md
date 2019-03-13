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
            "id": 3,
            "public_date": "2019-03-01T00:00:00",
            "expire_date": "2019-03-31T00:00:00",
            "highlight": 0,
            "status": 1,
            "user_group_id": 0,
            "reference": "https://vnexpress.net/",
            "created": "2019-03-09T14:41:00",
            "modified": "2019-03-09T14:41:00",
            "contents": [],
            "title": "Test tin tức",
            "brief": "Hello",
            "banner_img": "/uploads/files/annoucements/banners/TuyenDungCS1000x1000.png"
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