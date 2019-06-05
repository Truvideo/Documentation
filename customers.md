#### Notes: 
1- For all requests the {accountId} path parameter will be present.   


# Validate phone number
```
GET /api/v2/{{accountId}}/customer/validatePhoneNumber?number=+5493512894229
```

<details><summary>Response</summary>

```json
{
    "status": "Valid",
    "validNumber": "+5493512894229"
}
```
</details>
