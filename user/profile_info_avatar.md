# User Management: UPLOAD AVATAR

Use to upload avatar for current user.

**URL** : `/users/profile/avatar/`

**Method** : `POST`

**Content-Type** : multipart/form-data

**Auth required** : YES

**Data params**

**Data example**

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": "/uploads/files/avatar/user.png",
    "paging": [],
    "message": "Uploaded"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```