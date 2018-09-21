# Order Management: GET MONEY INFORMATION

Use to get order's money infomation.

**URL** : `/orders/moneys`

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
    "data": {
        "success_orders": {
            "cod": 0,
            "delivery_fee": 59000,
            "insurance_fee": 0,
            "transfer_fee": 0,
            "return_money": -49000,
            "total_order": 1,
            "detail": "/orders?order_status_id[in]=8"
        },
        "delivering_orders": {
            "cod": 0,
            "delivery_fee": 59000,
            "insurance_fee": 0,
            "transfer_fee": 0,
            "return_money": -49000,
            "total_order": 1,
            "detail": "/orders?order_status_id[in]=4,5,6,7"
        },
        "failed_orders": {
            "cod": 0,
            "delivery_fee": 59000,
            "insurance_fee": 0,
            "transfer_fee": 0,
            "return_money": -49000,
            "total_order": 1,
            "detail": "/orders?order_status_id[in]=9,10,11,12"
        }
    },
    "paging": {
        "total": 3,
        "total_page": 1
    },
    "message": "Moneys calculated"
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