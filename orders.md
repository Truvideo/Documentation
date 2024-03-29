#### Notes: 
1- For all requests the {accountId} path parameter will be present.   
2- For endpoints that returns paginated content, the path params {page} and {size} default values are 0 and 25 respectively. If you want to override the default values, add the path params to the request url. Example: /api/v2/{{accountId}}/repair-order/{{orderId}}?page=1&size=100 
## Get Order by Id

Look for an order with the provided id. 

```
GET /api/v2/{{accountId}}/repair-order/{{orderId}}
```

<details><summary>Response</summary>

```json
{
    "id": 1,
    "number": "1",
    "status": "Sent",
    "creationDate": 1550237332000,
    "updateDate": 1550241053000,
    "dealer": {
        "id": 41,
        "name": "Main Street Toyota",
        "status": "Active",
        "phone": "508-523-5151",
        "supportNumber": "(781) 819-0125",
        "partner": 2,
        "distributor": "distributorName",
        "timeZone": "America/New_York"
    },
    "advisor": {
        "id": 3056,
        "firstName": "firstName",
        "lastName": "lastName",
        "title": "title",
        "mobileNumber": "7813253414",
        "email": "email@email.com",
        "status": "Approved"
    },
    "customer": {
        "id": 1057833,
        "firstName": "Pablo",
        "lastName": "Chiban",
        "mobileNumber": "+5493512159262",
        "mobileStatus": "Valid",
        "email": "pablo.chiban@kenility.com"
    }
}
```
</details>

## Get Orders by Status

Returns orders by the provided status.

```
GET /api/v2/{{accountId}}/repair-order/status/{{STATUS_KEY}}
```

<details><summary>Response</summary>

```json
{
    "content": [
        {
            "id": 1,
            "number": "1",
            "status": "STATUS_SENT",
            "repairCondition": null,
            "originalAmount": null,
            "creationDate": 1550237332000,
            "updateDate": 1550241053000,
            "dealer": {
                "id": 41,
                "name": "Main Street Toyota",
                "status": "Active",
                "phone": "508-523-5151",
                "supportNumber": "(781) 819-0125",
                "partner": 2,
                "distributor": null,
                "timeZone": "America/New_York"
            },
            "advisor": {
                "id": 3056,
                "firstName": null,
                "lastName": null,
                "title": "",
                "mobileNumber": "7813253414",
                "email": null,
                "status": "Approved"
            },
            "customer": {
                "id": 1057833,
                "firstName": "Pablo",
                "lastName": "Chiban",
                "mobileNumber": "+5493512159262",
                "mobileStatus": "Valid",
                "email": "pablo.chiban@kenility.com"
            }
        }
    ],
    "totalPages": 1,
    "totalElements": 1,
    "last": true,
    "size": 25,
    "number": 0,
    "numberOfElements": 1,
    "first": true,
    "sort": null
}
```
</details>


## Create Order

Create a new order given the passed request
```
POST /api/v2/{accountId}/repair-order
```
<details><summary>Request</summary>

```json
{
	"number":"0303456-4",
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
    "status": "New",
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

## Update Order

Updates an order given the passed request
```
PUT /api/v2/{accountId}/repair-order/{repairOrderId}
```
### Query Params
* accountId - Dealer id
* repairOrderId

<details><summary>Request</summary>

```json
{
	"customerName": "Pepe",
	"customerLastName": "Argento",
	"mobileNumber": "+5493512894229",
	"email": "tomas.peirotti@gmail.com",
	"serviceAdvisor": 3056
}

```
</details>

<details><summary>Response</summary>

```json
{
    "id": 1,
    "number": "1",
    "status": "STATUS_SENT",
    "repairCondition": "condition",
    "creationDate": 1550237332000,
    "updateDate": 1559764386725,
    "dealer": {
        "id": 41,
        "name": "Main Street Toyota",
        "status": "Active",
        "phone": "508-523-5151",
        "supportNumber": "(781) 819-0125",
        "partner": 2,
        "distributor": "distributor",
        "timeZone": "America/New_York"
    },
    "advisor": {
        "id": 3056,
        "firstName": "firstName",
        "lastName": "lastName",
        "title": "title",
        "mobileNumber": "7813253414",
        "email": "email@email.com",
        "status": "Approved"
    },
    "customer": {
        "id": 1057833,
        "firstName": "Pepe",
        "lastName": "Argento",
        "mobileNumber": "+5493512894229",
        "mobileStatus": "Valid",
        "email": "tomas.peirotti@gmail.com"
    }
}
```
</details>

## Search Orders

Get orders by a search term that will be compared with: Customer first name, 
Customer last name, Job Service Number and Dealer name. It can be also filtered by a date interval.
There's also a query param to filter orders by status.
```
GET /api/v2/{accountId}/repair-order/search?creationDateFrom=1514813781000&creationDateTo=1575207381000&searchTerm=1&status=STATUS_NEW
```
<details><summary>Response</summary>

```json
{
    "content": [
        {
            "id": 266722,
            "number": "441062",
            "status": "STATUS_NEW",
            "repairCondition": "repairCondition",
            "originalAmount": 1,
            "creationDate": 1516223208000,
            "updateDate": 1516223257000,
            "dealer": {
                "id": 41,
                "name": "DEMO - Main Street Toyota",
                "status": "Inactive",
                "phone": "+15085235151",
                "supportNumber": "+17818190125",
                "partner": 2,
                "distributor": "distributor",
                "timeZone": "America/New_York"
            },
            "advisor": {
               "id": 3056,
               "firstName": "firstName",
               "lastName": "lastName",
               "title": "title",
               "mobileNumber": "7813253414",
               "email": "email@email.com",
               "status": "Approved"
            },
            "customer": {
                "id": 270843,
                "firstName": "Cherl",
                "lastName": "Daly",
                "mobileNumber": "+15086125134",
                "mobileStatus": "Valid",
                "email": "cdaly@email.com"
            }
        }
    ],
    "last": false,
    "totalElements": 43,
    "totalPages": 2,
    "size": 25,
    "number": 0,
    "sort": null,
    "first": true,
    "numberOfElements": 25
}
```
</details>