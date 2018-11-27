# Get  Token

Returns the custom authentication token for the device id
```
GET /chat/authentication/{deviceId}
```
<details><summary>Response</summary>

```json
{
   "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjEyMzQiLCJlbWFpbCI6ImpvaG4uZG9lQGdtYWlsLmNvbSIsImZpcnN0TmFtZSI6IkpvaG4iLCJsYXN0TmFtZSI6IkRvZSJ9.j1o-Fg9ds1A-uL5ypzlNOU8gttXCWBr71TAkFVg-uo0"     
}
```
</details>

# Get Contacts

Search contacts given the passed parameters
```
GET /chats/contacts?searchTerm={searchTerm}&deviceId={deviceId}&userId={userId}&dealerId={dealerId}&status={status}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (Name, Username, etc)
* status - User Status
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
     "userId": "c7IRzRc5dzOrU9LAYxU5IdStLAL2",
      "firstName": "Test",
      "lastName": "User",
     "avatar_url": "https:XXXXXXXX",
      "title": "Service Manager",
     "status": {
       "inOnline": false,
       "timestamp": 1542646212935
     }
   }
 ]
} 
```
</details>

# Create Channel

Create a new channel given the passed parameters 
```
POST /chat/channel
```
<details><summary>Request</summary>

```json
{
   "channelInfo": {
        "name": "channel1",
        "admin": "c7IRzRc5dzOrU9LAYxU5IdStLAL2"
      },
    "member": ["l4EqHph2AeeRAlnwlVb1GQY2neK2", "ucpvhwW8oOS2C2CA2EaAUQInFo32", "ucpvhwW8oOS2C2CA2EaAUQInFo32" ]
}
```
</details>

<details><summary>Response</summary>

```json
{
   "channelId": 627717061
}
```
</details>

# Update Channel

Update a channel given the passed parameters 
```
POST /chat/channel/{id}
```
<details><summary>Request</summary>

```json
{
   "channelInfo": {
        "name": "channel2",
        "admin": "c7IRzRc5dzOrU9LAYxU5IdStLAL2"
      },
    "member": ["ucpvhwW8oOS2C2CA2EaAUQInFo32", "ucpvhwW8oOS2C2CA2EaAUQInFo32" ]
}
```
</details>

<details><summary>Response</summary>

```json
{
   "channelId": 627717061
}
```
</details>
