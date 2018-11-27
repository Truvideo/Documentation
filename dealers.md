# Search Dealers

Search dealers given the passed parameters
```
GET /dealers?searchTerm={searchTerm}&status={status}&page={page}&size={size}
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
      "partner": {
        "id": 2,
        "name": "Truvideo",
        "phone": "(781) 123-123123",
        "email": "info@truvideo.com",
        "code": "tv"
      },
      "distributor": null,
      "status": {
        "value": "Active"
      },
      "phone": "55 (11) 123-123",
      "supportNumber": "123-123-123",
      "timezone": {
        "id": 12,
        "key": "TZ_CST",
        "value": "America/Chicago",
        "category": "TIMEZONE",
        "numberValue": -6
      }
    }
  ]
}
```
</details>

# Get Dealer by ID

Returns the dealer for the passed id
```
GET /dealers/{id}
```
<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": {
    "id": 2,
    "name": "Truvideo",
    "phone": "(781) 123-123123",
    "email": "info@truvideo.com",
    "code": "tv"
  },
  "distributor": null,
  "status": {
    "value": "Active"
  },
  "phone": "55 (11) 123-123",
  "supportNumber": "123-123-123",
  "timezone": {
    "id": 12,
    "key": "TZ_CST",
    "value": "America/Chicago",
    "category": "TIMEZONE",
    "numberValue": -6
  }
}
```
</details>

# Create Dealer

Create a new dealer given the passed request
```
POST /dealers
```
<details><summary>Request</summary>

```json
{
  "name": "A21 Motors",
  "partner": 2,
  "distributor": null,
  "status": "Active",
  "phone": "55 (11) 123-123",
  "supportNumber": "123-123-123",
  "timezone": "America/Chicago"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": {
    "id": 2,
    "name": "Truvideo",
    "phone": "(781) 123-123123",
    "email": "info@truvideo.com",
    "code": "tv"
  },
  "distributor": null,
  "status": {
    "value": "Active"
  },
  "phone": "55 (11) 123-123",
  "supportNumber": "123-123-123",
  "timezone": {
    "id": 12,
    "key": "TZ_CST",
    "value": "America/Chicago",
    "category": "TIMEZONE",
    "numberValue": -6
  }
}
```
</details>

# Update Dealer

Update a dealer given the passed request
```
PUT /dealers/{id}
```
<details><summary>Request</summary>

```json
{
  "name": "A21 Motors",
  "partner": 2,
  "distributor": null,
  "status": "Active",
  "phone": "55 (11) 123-123",
  "supportNumber": "123-123-123",
  "timezone": "America/Chicago"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 203,
  "name": "A21 Motors",
  "partner": {
    "id": 2,
    "name": "Truvideo",
    "phone": "(781) 123-123123",
    "email": "info@truvideo.com",
    "code": "tv"
  },
  "distributor": null,
  "status": {
    "value": "Active"
  },
  "phone": "55 (11) 123-123",
  "supportNumber": "123-123-123",
  "timezone": {
    "id": 12,
    "key": "TZ_CST",
    "value": "America/Chicago",
    "category": "TIMEZONE",
    "numberValue": -6
  }
}
```
</details>