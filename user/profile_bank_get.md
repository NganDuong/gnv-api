# User Management: PROFILE - BANK - GET

Use to get user's bank infomation.

**URL** : `/users/profile/banks/{id}`

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
            "support_bank_id": 1,
            "user_id": 5,
            "account_holder": "Nguyen Van Thai",
            "bank_name": "Ngân hàng Chính sách xã hội",
            "branch_name": "Quan 1",
            "bank_account_number": "01234136156789",
            "default_account": 1,
            "created": "2018-07-19T11:57:36+07:00",
            "modified": "2018-07-19T11:57:36+07:00",
            "bank_short_name": "NHCSXH/VBSP"
        }
    ],
    "paging": {
        "total": 1
    },
    "message": "Found bank(s)"
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
    "message": "bank not found"
}
```