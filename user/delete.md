# User Management: DELETE

Use to delete a user.

**URL** : `users/{id}`

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
    "message": "user not found"
}
```

OR

**Condition** : If required fields is empty or invaild.

**Code** : `400 BAD REQUEST`

**Content** :

{
    "success": false,
    "data": null,
    "paging": [],
    "message": "Unable to delete"
}