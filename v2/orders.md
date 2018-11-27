
# Create Order

Create a new order given the passed request
```
POST /api/v2/{dealerId}/repair-order/
```
<details><summary>Request</summary>

```json
{
	"number":"0303456-4",
	"serviceAdvisorId":3056,
	"customerName":"John",
	"customerLastName":"D",
	"mobileNumber":"+5493516650948",
	"email":"jd@gmail.com",
	"sendNotifications":true
}

```
</details>

<details><summary>Response</summary>

```json
{
    "id": 1008225,
    "number": "0303456-4",
    "creationDate": 1545147084414,
    "updateDate": 1545147085764,
    "dealer": {
        "id": 394,
        "name": "Dealer Xyz",
        "status": "Active"
    },
    "advisor": {
        "id": 3056,
        "firstName": "Administrator",
        "lastName": "TruVideo",
        "mobileNumber": "7813253414",
        "email": "admin@truvideo.com",
        "status": "Approved",
        "title": "",
        "dealers": [
            {
                "id": 394,
                "name": "Dealer Xyz",
                "status": "Active"
            }
        ]
    },
    "customer": {
        "id": 1021597,
        "firstName": "John",
        "lastName": "D",
        "mobileNumber": "+5493516650948",
        "mobileStatus": "Valid",
        "email": "jd@gmail.com"
    }
}
```
</details>
