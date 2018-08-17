# User Management: PROFILE - BANK - DELETE

Use to delete user's bank infomation.

**URL** : `/users/profile/banks/{id}`

**Method** : `DELETE`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

**Data example**

## Success Response

**Code** : `204 NO CONTENT`

**Content example**

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "bank not found"
}
```

OR

**Condition** : If required fields is empty or invaild.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "success": false,
    "data": null,
    "paging": [],
    "message": "Unable to delete"
}
```