# Shipper: UPLOAD PICKUP PHOTO

Use to upload a pickup photo.

**URL** : `/orders/pickup/upload/{id}`

**Method** : `POST`

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
    "data": "/uploads/files/orders/pickup/Screenshot from 2018-04-21 20-00-04.png",
    "paging": [],
    "message": "Uploaded photo"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `404 NOT FOUND`

**Content** :

```json

```