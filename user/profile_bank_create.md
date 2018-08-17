# User Management: PROFILE - BANK - CREATE

Use to create user's bank infomation.

**URL** : `/users/profile/banks`

**Method** : `POST`

**Content-Type** : application/json

**Auth required** : YES

**Data params**

    - _Required_

```json
{
  "account_holder": "[Account holder]",
  "support_bank_id": [support bank's id],  
  "branch_name": "[Bank's branch]",
  "bank_account_number": "[Bank account number]"
}
```

    - _Optional_

      - Note: If "support_bank_id" is empty, "bank_name" is required.

```json
{
  "bank_name": "[Bank's name]",
  "default_account": [0 (default) | 1],
}
```

**Data example**

```json
{
  "account_holder": "Nguyen Van Thai",
  "support_bank_id": 0,
  "bank_name": "Vietcombank",
  "branch_name": "Quan 1",
  "bank_account_number": "01234136156789"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "data": {
        "account_holder": "Nguyen Van Thai",
        "bank_name": "Vietcombank",
        "branch_name": "Quan 1",
        "bank_account_number": "01234136156789",
        "user_id": 10,
        "default_account": 1,
        "created": "2018-07-19T13:37:54+07:00",
        "modified": "2018-07-19T13:37:54+07:00",
        "id": 5
    },
    "paging": [],
    "message": "Created bank"
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
    "message": "Unable to create bank"
}
```