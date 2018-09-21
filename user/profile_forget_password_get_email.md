# User Management: PROFILE - FORGET PASSWORD - GET EMAIL

Use to update user's infomation.

**URL** : `users/verify?email={email}`

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
    "data": [],
    "paging": [],
    "message": "An email has been sent to ngan.duong1995@gmail.com"
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
    "message": "User not found"
}
```