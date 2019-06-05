#### Notes: 
1- For all requests the {accountId} path parameter will be present.   
2- For endpoints that returns paginated content, the path params {page} and {size} default values are 0 and 25 respectively. If you want to override the default values, add the path params to the request url. Example: /api/v2/{{accountId}}/user?page=1&size=100

# Get all users

Gets all users of an account.
```
GET /api/v2/{{accountId}}/user
```

<details><summary>Response</summary>

```json
{
    "content": [
        {
            "id": 3056,
            "firstName": "Administrator",
            "lastName": "TruVideo",
            "title": "title",
            "mobileNumber": "7813253414",
            "email": "admin@truvideo.com",
            "status": "Approved"
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