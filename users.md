
# Search Users

Search orders given the passed parameters
```
GET /api/v2/{accountId}/users?searchTerm={searchTerm}&status={status}&createdDateFrom={createdDateFrom}&createdDateTo={createdDateTo}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (first name, last name, email, etc)
* status - User Status
* createdDateFrom - User Creation From
* createdDateTo - User Creation To
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
      "id": 3511,
	  "firstName": "John",
	  "lastName": "Doe",
	  "title": "Technician",
	  "email": "jonh.doe@gmail.com",
	  "mobileNumber": "+12025550185",
      "status": "Approved",
      "dealers": [
        {
          "id": 553,
          "name": "Baker Cadillac",
          "partner": 1,
          "distributor": 2,
          "status": "Active",
          "phone": "+12025550119",
          "supportNumber": "+12025550145",
          "timeZone": "America/New_York"
        },
        {
          "id": 549,
          "name": "AutoFair Subaru",
          "partner": 1,
          "distributor": 2,
          "status": "Active",
          "phone": "+12025550343",
          "supportNumber": "+12025550303",
          "timeZone": "America/New_York"
        }
      ],
      "roles": [
        "Service App",
        "Service Dashboard"
      ]
    }
  ]
}
```
</details>

# Get User

Get a user given the passed id
```
GET /api/v2/{accountId}/users/{userId}
```

<details><summary>Response</summary>

```json
{
  "id": 3511,
  "firstName": "John",
  "lastName": "Doe",
  "title": "Technician",
  "email": "jonh.doe@gmail.com",
  "mobileNumber": "+12025550185",
  "status": "Approved",
  "dealers": [
     {
       "id": 553,
       "name": "Baker Cadillac",
       "partner": 1,
       "distributor": 2,
       "status": "Active",
       "phone": "+12025550119",
       "supportNumber": "+12025550145",
       "timeZone": "America/New_York"
     },
     {
       "id": 549,
       "name": "AutoFair Subaru",
       "partner": 1,
       "distributor": 2,
       "status": "Active",
       "phone": "+12025550343",
       "supportNumber": "+12025550303",
       "timeZone": "America/New_York"
     }
   ],
   "roles": [
     "Service App",
     "Service Dashboard"
   ]
}
```
</details>


# Create User

Create a new user given the passed request
```
POST /api/v2/{accountId}/users
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "title": "Technician",
  "email": "jonh.doe@gmail.com",
  "mobileNumber": "+12025550185",
  "status": "Approved",
  "dealers": [
     553,
     549
   ],
   "roles": [
     "Service App",
     "Service Dashboard"
   ]
}
```
</details>

<details><summary>Response</summary>

```json
{
  "id": 3511,
  "firstName": "John",
  "lastName": "Doe",
  "title": "Technician",
  "email": "jonh.doe@gmail.com",
  "mobileNumber": "+12025550185",
  "status": "Approved",
  "dealers": [
     {
       "id": 553,
       "name": "Baker Cadillac",
       "partner": 1,
       "distributor": 2,
       "status": "Active",
       "phone": "+12025550119",
       "supportNumber": "+12025550145",
       "timeZone": "America/New_York"
     },
     {
       "id": 549,
       "name": "AutoFair Subaru",
       "partner": 1,
       "distributor": 2,
       "status": "Active",
       "phone": "+12025550343",
       "supportNumber": "+12025550303",
       "timeZone": "America/New_York"
     }
   ],
   "roles": [
     "Service App",
     "Service Dashboard"
   ]
}
```
</details>

# Update User

Updates a user given the passed request
```
PUT /api/v2/{accountId}/users/{id}
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "title": "Technician",
  "email": "jonh.doe@gmail.com",
  "mobileNumber": "+12025550185",
  "status": "Approved",
  "dealers": [
     553
   ],
   "roles": [
     "Service App"
   ]
}
```
</details>

<details><summary>Response</summary>

```json
{
  "id": 3511,
  "firstName": "John",
  "lastName": "Doe",
  "title": "Technician",
  "email": "jonh.doe@gmail.com",
  "mobileNumber": "+12025550185",
  "status": "Approved",
  "dealers": [
     {
       "id": 553,
       "name": "Baker Cadillac",
       "partner": 1,
       "distributor": 2,
       "status": "Active",
       "phone": "+12025550119",
       "supportNumber": "+12025550145",
       "timeZone": "America/New_York"
     }
   ],
   "roles": [
     "Service App"
   ]
}
```
</details>
