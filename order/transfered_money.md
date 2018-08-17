# Order Management: GET TRANSFERED MONEYS INFORMATION

Use to get order's money infomation.

**URL** : `orders/transferedMoneys`

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
            "id": 5,
            "bill_code": "B-1531729617",
            "amount": 1178000,
            "validate_code": "16466666",
            "confirm_date": "2018-07-16T17:52:24",
            "cross_check_date": "2018-07-16T15:26:57",
            "note": "",
            "created": "2018-07-16T15:26:57",
            "user_id": 5,
            "account_holder": "Nguyễn Thị An",
            "bank_name": "Vietcombank",
            "branch_name": "Quan 1",
            "bank_account_number": "01234136156789",
            "customer_name": "customer",
            "customer_code": "G1527473478",
            "cod": 570000,
            "delivery_fee": 57000,
            "insurance_fee": 0,
            "return_fee": 0,
            "transfer_fee": 0,
            "return_order": 0,
            "success_order": 3,
            "detail": "/orders?id[in]=106,103,104"
        },
        {
            "id": 10,
            "bill_code": "B-1531794968",
            "amount": 147000,
            "validate_code": "DS012345678",
            "confirm_date": "2018-07-17T17:11:18",
            "cross_check_date": "2018-07-17T09:36:08",
            "note": "",
            "created": "2018-07-17T09:36:08",
            "user_id": 5,
            "account_holder": "Nguyễn Thị An",
            "bank_name": "Vietcombank",
            "branch_name": "Quan 1",
            "bank_account_number": "01234136156789",
            "customer_name": "customer",
            "customer_code": "G1527473478",
            "cod": 200000,
            "delivery_fee": 174000,
            "insurance_fee": 0,
            "return_fee": 0,
            "transfer_fee": 0,
            "return_order": 0,
            "success_order": 6,
            "detail": "/orders?id[in]=108,135,136,137,138,139"
        }
    ],
    "paging": {
        "total": 2
    },
    "message": "Founds"
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
    "message": "order not found"
}
```