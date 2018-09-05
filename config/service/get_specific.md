# Config Management: DELIVERY SERVICE - GET 

Use to get user's bank infomation.

**URL** : `/configs/orders/deliveries/services?sender_location_id={id}&receiver_location_id={id}`

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
            "id": 1,
            "name": "Chuẩn",
            "group_location_type_id": 1,
            "location_type_id": 1,
            "description": "",
            "created_before": "2018-08-31T10:00:00+07:00",
            "delivery_day": 0,
            "delivery_before": "2018-08-31T18:00:00+07:00",
            "standard_weight": 3000,
            "price": 19000,
            "extra_weight": 500,
            "extra_weight_price": 3000,
            "created": "2018-07-03T21:22:00+07:00",
            "modified": "2018-07-03T21:22:00+07:00",
            "group_location_type": {
                "id": 1,
                "name": "Nội tỉnh",
                "created": "2018-08-30T17:00:00+07:00",
                "modified": "2018-08-30T17:00:00+07:00"
            },
            "location_type": {
                "id": 1,
                "name": "Nội Thành",
                "created": "2018-06-28T03:00:00+07:00",
                "modified": "2018-06-28T03:00:00+07:00"
            }
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found service(s)"
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
    "message": "service not found"
}
```