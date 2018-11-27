# Get Access Token

Returns an access token for the passed credentials 
```
POST /authentication
```
<details><summary>Request</summary>

```json
{
  "email":"john.doe@gmail.com",
  "password":"123123123"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEyMzQiLCJlbWFpbCI6ImpvaG4uZG9lQGdtYWlsLmNvbSIsImZpcnN0TmFtZSI6IkpvaG4iLCJsYXN0TmFtZSI6IkRvZSJ9.j1o-Fg9ds1A-uL5ypzlNOU8gttXCWBr71TAkFVg-uo0"     
}
```
</details>
