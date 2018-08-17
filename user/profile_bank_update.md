# User Management: PROFILE - BANK - UPDATE

Use to create user's bank infomation.

**URL** : `/users/profile/banks/{id}`

**Method** : `PATCH`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Optional_

        - Note: If "support_bank_id" is null or 0, "bank_name" is required.

```json
{
  "account_holder": "[Account holder]",
  "support_bank_id": [support bank's id],
  "bank_name": "[Bank's name]",
  "branch_name": "[Bank's branch]",
  "bank_account_number": "[Bank account number]"
  "default_account": [0 (default) | 1],
}
```

**Data example**

```json
{
  "default_account": 1
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "id": 5,
        "support_bank_id": 0,
        "user_id": 10,
        "account_holder": "Nguyen Van Thai",
        "bank_name": "Vietcombank",
        "branch_name": "Quan 1",
        "bank_account_number": "01234136156789",
        "default_account": 1,
        "created": "2018-07-19T13:37:54+07:00",
        "modified": "2018-07-19T13:42:21+07:00"
    },
    "paging": [],
    "message": "Updated bank"
}
```

## Error Response

**Condition** : If required fields is empty or invaild.

**Code** : `409 CONFLICT`

**Content** :

```json
{
    "success": false,
    "data": {
        "user_id": {
            "_isUnique": "This user_id, account_holder, support_bank_id, branch_name & bank_account_number combination has already been used."
        }
    },
    "paging": [],
    "message": "Unable to update bank"
}
```

Or

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