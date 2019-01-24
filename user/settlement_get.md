# User Management: GET SETTLEMENTS INFORMATION

Use to get user's settlements infomation.

**URL** : `/users/settlements/open`

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
            "name": "Current settlements",
            "details": [
                {
                    "name": "total collected",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total cod",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total deliver fees",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total insurance fees",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total transfer fees",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total settlement amount",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total return fees",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "total orders",
                    "value": 0,
                    "type": 0
                },
                {
                    "name": "order details",
                    "value": "/orders?id[in]=",
                    "type": 1
                }
            ]
        }
    ],
    "paging": [],
    "message": "Found open settlements"
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
    "message": "settlements not found"
}
```