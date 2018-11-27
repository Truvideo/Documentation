# Search Users

Search orders given the passed parameters
```
GET /users?searchTerm={searchTerm}&status={status}&createdDateFrom={createdDateFrom}&createdDateTo={createdDateTo}&page={page}&size={size}
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
      "email": "jonh.doe@gmail.com",
      "title": "Technician",
      "status": "ACTIVE",
      "dealers": [
        1,
        2
      ],
      "roles": [
        "USER",
        "ADMIN"
      ]
    }
  ]
}
```
</details>

# Create User

Create a new user given the passed request
```
POST /users
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "jonh.doe@gmail.com",
  "title": "Technician",
  "status": "ACTIVE",
  "dealers": [
    1,
    2
  ],
  "roles": [
    "USER",
    "ADMIN"
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
  "email": "jonh.doe@gmail.com",
  "title": "Technician",
  "status": "ACTIVE",
  "dealers": [
    1,
    2
  ],
  "roles": [
    "USER",
    "ADMIN"
  ]
}
```
</details>

# Update User

Updates a user given the passed request
```
PUT /users/{id}
```
<details><summary>Request</summary>

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "jonh.doe@gmail.com",
  "title": "Technician",
  "status": "ACTIVE",
  "dealers": [
    1,
    2
  ],
  "roles": [
    "USER",
    "ADMIN"
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
  "email": "jonh.doe@gmail.com",
  "title": "Technician",
  "status": "ACTIVE",
  "dealers": [
    1,
    2
  ],
  "roles": [
    "USER",
    "ADMIN"
  ]
}
```
</details>