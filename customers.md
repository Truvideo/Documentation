#### Notes: 
1- For all requests the {accountId} path parameter will be present.   


# Validate phone number
```
POST /api/v2/{{accountId}}/customer/validatePhoneNumber
```
<details><summary>Request</summary>

```json
{
    "phone": "+5493512894229"
}
```
</details>

<details><summary>Response</summary>

```json
{
    "status": "Valid",
    "validNumber": "+5493512894229"
}
```
</details>
