# Config Management: PROMOTION - GET USABLE PROMOTIONS FOR A USER

Use to get usable promotions.

**URL** : `/configs/promotions/usable?sender_location_id={id}&receiver_location_id={id}`

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
            "name": "Promotion T11",
            "description": "Using within December",
            "code": "DONGGIA5K",
            "method": 2,
            "rate": 5000,
            "public_date": "2018-10-27T00:00:00+07:00",
            "expire_date": "2018-10-31T00:00:00+07:00",
            "use_in_total": 0
        }
    ],
    "paging": {
        "total": 1,
        "total_page": 1
    },
    "message": "Found promotion(s)"
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
    "message": "promotion not found"
}
```