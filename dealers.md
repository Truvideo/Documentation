# Search Dealers

Search dealers given the passed parameters
```
GET /api/v2/{accountId}/dealers?searchTerm={searchTerm}&status={status}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (Name, Main Contact, etc)
* status - Dealer Status
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
      "id": 203,
      "name": "A21 Motors",
      "partner": 2,
      "distributor": 528,
      "status": "Active",
      "phone": "508-523-5151",
      "supportNumber": "(781) 819-0125",
      "timezone": "America/Chicago"
    }
  ]
}
```
</details>

# Get Dealer by ID

Returns the dealer for the passed id
```
GET /api/v2/{accountId}/dealers/{id}
```
<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": 2,
  "distributor": 528,
  "status": "Active",
  "phone": "508-523-5151",
  "supportNumber": "(781) 819-0125",
  "timezone": "America/Chicago"
}
```
</details>

# Create Dealer

Create a new dealer given the passed request
```
POST /api/v2/{accountId}/dealers
```
<details><summary>Request</summary>

```json
{
  "name": "A21 Motors",
  "partner": 2,
  "distributor": 528,
  "status": "Active",
  "phone": "508-523-5151",
  "supportNumber": "(781) 819-0125",
  "timezone": "America/Chicago"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": 2,
  "distributor": 528,
  "status": "Active",
  "phone": "508-523-5151",
  "supportNumber": "(781) 819-0125",
  "timezone": "America/Chicago"
}
```
</details>

# Update Dealer

Update a dealer given the passed request
```
PUT /api/v2/{accountId}/dealers/{id}
```
<details><summary>Request</summary>

```json
{
  "name": "A21 Motors",
  "partner": 2,
  "distributor": 528,
  "status": "Active",
  "phone": "508-523-5151",
  "supportNumber": "(781) 819-0125",
  "timezone": "America/Chicago"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": 2,
  "distributor": 528,
  "status": "Active",
  "phone": "508-523-5151",
  "supportNumber": "(781) 819-0125",
  "timezone": "America/Chicago"
}
```
</details>