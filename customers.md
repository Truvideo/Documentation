# Search Customers

Search customers given the passed parameters
```
GET /api/v2/{accountId}/customers?searchTerm={searchTerm}&status={status}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (First Name, Last Name, mobile number, email, etc)
* status - Customer Status
* page - Page number 0 based
* size - Number of records returned (defaults to 25)
<details><summary>Response</summary>

```json
{
  "last": false,
  "totalElements": 20,
  "totalPages": 7,
  "size": 3,
  "number": 0,
  "sort": null,
  "first": true,
  "numberOfElements": 3,
  "content": [
    {
      "id": 593,
      "createDate": 1550674031282,
      "updateDate": 1550674031282,
      "firstName": "John",
      "lastName": "McAllister",
      "mobileNumber": "(781) 839-0224",
      "email": "john.mcallister@gmail.com",
      "mobileStatus": "Active",
      "cdkId": "9283",
      "sisId": "5662",
      "name": "John McAllister",
      "formattedName": "McAllister , John",
      "completeName": "John  McAllister"
    }
  ]
}
```
</details>

# Get Customer by ID

Returns the customer for the passed id
```
GET /api/v2/{accountId}/customers/{id}
```
<details><summary>Response</summary>

```json
{
  "id": 593,
  "createDate": 1550674031282,
  "updateDate": 1550674031282,
  "firstName": "John",
  "lastName": "McAllister",
  "mobileNumber": "(781) 839-0224",
  "email": "john.mcallister@gmail.com",
  "mobileStatus": "Active",
  "cdkId": "9283",
  "sisId": "5662",
  "name": "John McAllister",
  "formattedName": "McAllister , John",
  "completeName": "John  McAllister"
}
```
</details>

# Create Customer

Create a new dealer given the passed request
```
POST /api/v2/{accountId}/customers
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "McAllister",
  "mobileNumber": "(781) 839-0224",
  "email": "john.mcallister@gmail.com",
  "mobileStatus": "Active",
  "cdkId": "9283",
  "sisId": "5662",
  "name": "John McAllister",
  "formattedName": "McAllister , John",
  "completeName": "John  McAllister"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 593,
  "createDate": 1550674031282,
  "updateDate": 1550674031282,
  "firstName": "John",
  "lastName": "McAllister",
  "mobileNumber": "(781) 839-0224",
  "email": "john.mcallister@gmail.com",
  "mobileStatus": "Active",
  "cdkId": "9283",
  "sisId": "5662",
  "name": "John McAllister",
  "formattedName": "McAllister , John",
  "completeName": "John  McAllister"
}
```
</details>

# Update Customer

Update a customer given the passed request
```
PUT /api/v2/{accountId}/customers/{id}
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "McAllister",
  "mobileNumber": "(781) 839-0224",
  "email": "john.mcallister@gmail.com",
  "mobileStatus": "Active",
  "cdkId": "9283",
  "sisId": "5662",
  "name": "John McAllister",
  "formattedName": "McAllister , John",
  "completeName": "John  McAllister"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 593,
  "createDate": 1550674031282,
  "updateDate": 1550674031282,
  "firstName": "John",
  "lastName": "McAllister",
  "mobileNumber": "(781) 839-0224",
  "email": "john.mcallister@gmail.com",
  "mobileStatus": "Active",
  "cdkId": "9283",
  "sisId": "5662",
  "name": "John McAllister",
  "formattedName": "McAllister , John",
  "completeName": "John  McAllister"
}
```
</details>
