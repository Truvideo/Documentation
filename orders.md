# Search Orders

Search orders given the passed parameters
```
GET /orders?searchTerm={searchTerm}&status={status}&dealerIds={dealerIds}&createdDateFrom={createdDateFrom}&createdDateTo={createdDateTo}&customerId={customerId}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (dealer, customer, order items)
* status - Order Status
* dealerIds - Dealer Id comma separated
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
      "id": 1005887,
      "dateOrdered": "11/21/2018",
      "securityKey": "E3T7Wn",
      "securityPinIncluded": null,
      "userReviewed": null,
      "customer": {
        "id": 1019259,
        "firstName": "Anna",
        "lastName": "Vuit",
        "mobileNumber": "",
        "email": "ssa4test@gmail.com",
        "mobileStatus": null,
        "cdkId": null,
        "sisId": null,
        "formattedName": "Vuit , Anna",
        "name": "Anna Vuit"
      },
      "dealerId": 394,
      "orderStatus": {
        "id": 2,
        "key": "STATUS_NEW",
        "value": "New",
        "category": "ORDER_STATUS",
        "numberValue": 1,
        "parentKey": "",
        "parentKeyString": ""
      },
      "previousStatus": null,
      "orderStatusKey": "STATUS_NEW",
      "owner": {
        "id": 3056,
        "firstName": "Administrator",
        "lastName": "TruVideo",
        "middleName": null,
        "emailAddress": "admin@truvideo.com",
        "office": "394",
        "pin": "123456",
        "title": "",
        "mobileNumber": "7813253414"
      }
    }
  ]
}
```
</details>

# Create Order

Create a new order given the passed request
```
POST /orders
```
<details><summary>Request</summary>

```json
{
  "number": 242432,
  "customerId": 1019259,
  "dealerId": 394,
  "status": "STATUS_NEW",
  "advisorId": 12403,
  "technicianId": 1123,
  "securityPin": true
}

```
</details>

<details><summary>Response</summary>

```json
{
      "id": 1005887,
      "dateOrdered": "11/21/2018",
      "securityKey": "E3T7Wn",
      "securityPinIncluded": null,
      "userReviewed": null,
      "customer": {
        "id": 1019259,
        "firstName": "Anna",
        "lastName": "Vuit",
        "mobileNumber": "",
        "email": "ssa4test@gmail.com",
        "mobileStatus": null,
        "cdkId": null,
        "sisId": null,
        "formattedName": "Vuit , Anna",
        "name": "Anna Vuit"
      },
      "dealerId": 394,
      "orderStatus": {
        "id": 2,
        "key": "STATUS_NEW",
        "value": "New",
        "category": "ORDER_STATUS",
        "numberValue": 1,
        "parentKey": "",
        "parentKeyString": ""
      },
      "previousStatus": null,
      "orderStatusKey": "STATUS_NEW",
      "owner": {
        "id": 3056,
        "firstName": "Administrator",
        "lastName": "TruVideo",
        "middleName": null,
        "emailAddress": "admin@truvideo.com",
        "office": "394",
        "pin": "123456",
        "title": "",
        "mobileNumber": "7813253414"
      }
    }
```
</details>

# Update Order

Updates an order given the passed request
```
PUT /orders/{id}
```
<details><summary>Request</summary>

```json
{
  "number": 242432,
  "customerId": 1019259,
  "dealerId": 394,
  "status": "STATUS_NEW",
  "advisorId": 12403,
  "technicianId": 1123,
  "securityPin": true
}

```
</details>

<details><summary>Response</summary>

```json
{
      "id": 1005887,
      "dateOrdered": "11/21/2018",
      "securityKey": "E3T7Wn",
      "securityPinIncluded": null,
      "userReviewed": null,
      "customer": {
        "id": 1019259,
        "firstName": "Anna",
        "lastName": "Vuit",
        "mobileNumber": "",
        "email": "ssa4test@gmail.com",
        "mobileStatus": null,
        "cdkId": null,
        "sisId": null,
        "formattedName": "Vuit , Anna",
        "name": "Anna Vuit"
      },
      "dealerId": 394,
      "orderStatus": {
        "id": 2,
        "key": "STATUS_NEW",
        "value": "New",
        "category": "ORDER_STATUS",
        "numberValue": 1,
        "parentKey": "",
        "parentKeyString": ""
      },
      "previousStatus": null,
      "orderStatusKey": "STATUS_NEW",
      "owner": {
        "id": 3056,
        "firstName": "Administrator",
        "lastName": "TruVideo",
        "middleName": null,
        "emailAddress": "admin@truvideo.com",
        "office": "394",
        "pin": "123456",
        "title": "",
        "mobileNumber": "7813253414"
      }
    }
```
</details>