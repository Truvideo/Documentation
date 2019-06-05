# Login

Logs the user into the system and returns an access token for the passed credentials.
```
POST /api/v2/authentication/login
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

# Logout

Logs the user out of the system.
```
POST /api/v2/authentication/logout
```
Empty request and response body.  
**Note**: Authentication header must be present in the request.
