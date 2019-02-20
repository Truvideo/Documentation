# Search Orders

Search orders given the passed parameters
```
GET /api/v2/{accountId}/repair-order?searchTerm={searchTerm}&status={status}&accountIds={accountIds}&createdDateFrom={createdDateFrom}&createdDateTo={createdDateTo}&customerId={customerId}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (dealer, customer, order items)
* status - Order Status
* accountIds - Account Id comma separated
* createdDateFrom - Order Creation From
* createdDateTo - Order Creation To
* customerId - Customer Id
* page - Page number 0 based
* size - Number of records returned (defaults to 25)
<details><summary>Response</summary>

```json
{
  "last": false,
  "totalElements": 13,
  "totalPages": 2,
  "size": 7,
  "number": 0,
  "sort": null,
  "first": true,
  "numberOfElements": 7,
  "content": [
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
  ]
}
```
</details>

# Get Order by ID

Returns the order for the passed id
```
GET /api/v2/{accountId}/repair-order/{repairOrderId}
```
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


# Create Order

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

# Update Order

Updates an order given the passed request
```
PUT /api/v2/{accountId}/repair-order/{repairOrderId}
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