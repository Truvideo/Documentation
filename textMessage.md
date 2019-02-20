# Search Text Message

Search text messages given the passed parameters
```
GET /api/v2/{accountId}/textMessages?searchTerm={searchTerm}&status={status}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across multiple fields (customer, fromNumber, toNumber, orderId, dealerId, etc)
* status - Customer Status
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
      "id": 4355,
      "createDate": 1550697081222,
      "updateDate": 1550697081222,
      "textConversation": 436,
      "customer": 834,
      "dateTimeSent": 1550697081222,
      "status": "ACTIVE",
      "direction": "outbound",
      "message": "Please review the video link I texted earlier.",
      "smsMessageSid": "SM4a8de52de4314849a4e6ccb3b4e510f5",
      "customersMobileNumber": "508-523-5151",
      "orderId": 55,
      "dealerId": 41,
      "serviceAdvisor": 223,
      "from": "(781) 819-0125",
      "to": "508-523-5151",
      "conversation": 877,
      "displayDateTimeSent": "12:11PM/20-Feb",
      "displayMessageTimeDateSent": "12:11PM (02/20/19)",
      "displayTimeSent": "12:11PM",
      "displayDateSent": "Today",
      "displayMessageDate": "20-Feb, 12:11PM",
      "initialOutboundFullMessage": "From Mazda: Please review the video link I texted earlier. Reply STOP to opt out."
    }
  ]
}
```
</details>

# Get Text Message by ID

Returns the text message for the passed id
```
GET /api/v2/{accountId}/textMessages/{id}
```
<details><summary>Response</summary>

```json
{
  "id": 4355,
  "createDate": 1550697081222,
  "updateDate": 1550697081222,
  "textConversation": 436,
  "customer": 834,
  "dateTimeSent": 1550697081222,
  "status": "ACTIVE",
  "direction": "outbound",
  "message": "Please review the video link I texted earlier.",
  "smsMessageSid": "SM4a8de52de4314849a4e6ccb3b4e510f5",
  "customersMobileNumber": "508-523-5151",
  "orderId": 55,
  "dealerId": 41,
  "serviceAdvisor": 223,
  "from": "(781) 819-0125",
  "to": "508-523-5151",
  "conversation": 877,
  "displayDateTimeSent": "12:11PM/20-Feb",
  "displayMessageTimeDateSent": "12:11PM (02/20/19)",
  "displayTimeSent": "12:11PM",
  "displayDateSent": "Today",
  "displayMessageDate": "20-Feb, 12:11PM",
  "initialOutboundFullMessage": "From Mazda: Please review the video link I texted earlier. Reply STOP to opt out."
}
```
</details>

# Create Text Message

Create a new text message given the passed request
```
POST /api/v2/{accountId}/textMessages
```
<details><summary>Request</summary>

```json
{
  "customer": 834,
  "message": "Please review the video link I texted earlier."
  "customersMobileNumber": "508-523-5151",
  "orderId": 55,
  "dealerId": 41,
  "serviceAdvisor": 223,
  "from": "(781) 819-0125",
  "to": "508-523-5151"
}

```
</details>

<details><summary>Response</summary>

```json
{
  "id": 4355,
  "createDate": 1550697081222,
  "updateDate": 1550697081222,
  "textConversation": 436,
  "customer": 834,
  "dateTimeSent": 1550697081222,
  "status": "ACTIVE",
  "direction": "outbound",
  "message": "Please review the video link I texted earlier.",
  "smsMessageSid": "SM4a8de52de4314849a4e6ccb3b4e510f5",
  "customersMobileNumber": "508-523-5151",
  "orderId": 55,
  "dealerId": 41,
  "serviceAdvisor": 223,
  "from": "(781) 819-0125",
  "to": "508-523-5151",
  "conversation": 877,
  "displayDateTimeSent": "12:11PM/20-Feb",
  "displayMessageTimeDateSent": "12:11PM (02/20/19)",
  "displayTimeSent": "12:11PM",
  "displayDateSent": "Today",
  "displayMessageDate": "20-Feb, 12:11PM",
  "initialOutboundFullMessage": "From Mazda: Please review the video link I texted earlier. Reply STOP to opt out."
}
```
</details>
