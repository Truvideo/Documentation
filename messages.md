# Get Messages by Conversation

Search messages given the passed conversation's id 
```
GET /api/v2/{{accountId}}/messages/conversations/{{conversationId}}?page={{page}}&size={{size}}
```

### Query Params
* accountId - Dealer id
* conversationId - Conversation's id
* page - Page number 0 based
* size - Number of records returned (defaults to 25)
<details><summary>Response</summary>

```json
{
    "id": 532170,
    "accountId": 463,
    "accountName": "Test Dealer",
    "ownerId": 8665,
    "ownerName": "Stephanie",
    "orderId": 1359190,
    "orderDescription": "84145",
    "customerId": 1380832,
    "customerMobile": "+14055355870",
    "customerName": "JUAN , PEREZ",
    "status": "Open",
    "type": "REPAIR_ORDER",
    "lastTextMessage": {
        "id": 1576828,
        "direction": "inbound",
        "sender": "+14055355870",
        "receiver": "+15125809043",
        "timestamp": "2019-08-07T18:04:56.000Z",
        "message": ""
    },
    "messages": {
        "content": [
            {
                "id": 914190,
                "direction": "inbound",
                "sender": "+15125809043",
                "receiver": "+15125809043",
                "timestamp": "2019-02-26T03:38:13.000Z",
                "message": "Thank you Stephanie"
            },
            {
                "id": 914192,
                "direction": "outbound",
                "sender": "+14055355870",
                "receiver": "+14055355870",
                "timestamp": "2019-02-26T03:39:20.000Z",
                "message": "You're welcome!  I hope you get to leave soon and enjoy the evening.  I will contact you tomorrow."
            },
            {
                "id": 915631,
                "direction": "inbound",
                "sender": "+15125809043",
                "receiver": "+15125809043",
                "timestamp": "2019-02-26T19:39:47.000Z",
                "message": "No worries. Thanks"
            }
        ],
        "totalPages": 10,
        "totalElements": 30,
        "last": false,
        "size": 3,
        "number": 0,
        "sort": null,
        "first": true,
        "numberOfElements": 3
    }
}
```
</details>

# Create Message for Conversation

Create a new message given the passed request
```
POST /api/v2/{{accountId}}/messages
```
### Query Params
* accountId - Dealer id

### Comments
* conversationId is null: for a new Conversation
* conversationId is not null: add message to Conversation related.

<details><summary>Request</summary>

```json
{
    "conversationId": null,
    "source": "CONVERSATION",
    "sender": 8665,
    "order": 1359190,
    "mobile": "+14055355870",
    "message": "Test"
}

```
</details>

<details><summary>Response</summary>

* HTTP Status: 203 Created
* HTTP Header: Location /api/v2/{{accountId}}/messages/conversations/{{conversationId}}

</details>

# Search Conversations

Get conversations by a search term that will be compared with: Customer first name, 
Customer last name, Job Service Number and Dealer name. It can be also filtered by a date interval.
There's also a query param to filter conversations by status.
```
GET /api/v2/{{accountId}}/messages/conversations?orderId={{orderId}}&customerId={{customerId}}&status={{status}}&searchTerm={{searchTerm}}&page={{page}}&size={{size}}
```
### Query Params
* accountId - Dealer id
* orderId - Order Id related to Conversation
* customerId - Customer Id related to Conversation
* status - Conversation status (ACTIVE, RESPONDED, CLOSED) 
* search term - that will be compared with: Customer first name, Customer last name, Customer mobile, Owner Number and Dealer name
* page - Page number 0 based
* size - Number of records returned (defaults to 25)
<details><summary>Response</summary>

```json
{
    "content": [
        {
            "id": 532170,
            "accountId": 463,
            "accountName": "Test Dealer",
            "ownerId": 8665,
            "ownerName": "Stephanie",
            "orderId": 1359190,
            "orderDescription": "84145",
            "customerId": 1380832,
            "customerMobile": "+14055355870",
            "customerName": "JUAN , PEREZ",
            "status": "Open",
            "type": "REPAIR_ORDER",
            "lastTextMessage": {
                "id": 1576828,
                "direction": "inbound",
                "sender": "+14055355870",
                "receiver": "+15125809043",
                "timestamp": "2019-08-07T18:04:56.000Z",
                "message": ""
            }
        }
    ],
    "last": false,
    "totalElements": 43,
    "totalPages": 2,
    "size": 25,
    "number": 0,
    "sort": null,
    "first": true,
    "numberOfElements": 25
}
```
</details>
