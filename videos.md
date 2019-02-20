# Search Videos

Search video given the passed parameters
```
GET /api/v2/{accountId}/videos?searchTerm={searchTerm}&dealerId={dealerId}&orderId={orderId}&page={page}&size={size}
```

### Query Params
* searchTerm - Searches across Title and Description fields
* dealerId - The dealer Id
* dealerId - The order Id
* page - Page number 0 based
* size - Number of records returned (defaults to 25)
<details><summary>Response</summary>

```json
{
   "last":false,
   "totalElements":20,
   "totalPages":7,
   "size":3,
   "number":0,
   "sort":null,
   "first":true,
   "numberOfElements":3,
   "content":[
      {
         "id":594178,
         "title":"Video #1",
         "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
         "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
         "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
         "length":71517,
         "lastViewedDate":1550694192,
         "playedDuration":71517,
         "uploaderId":3511,
         "orderId":1008225
      }
   ]
}
```
</details>

# Get Video by ID

Returns the video for the passed id
```
GET /api/v2/{accountId}/videos/{id}
```
<details><summary>Response</summary>

```json
{
   "id":594178,
   "title":"Video #1",
   "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
   "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
   "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
   "length":71517,
   "lastViewedDate":1550694192,
   "playedDuration":71517,
   "uploaderId":3511,
   "orderId":1008225
}
```
</details>

# Create Video

Create a new video given the passed request
```
POST /api/v2/{accountId}/videos
```
<details><summary>Request</summary>

```json
{
   "title":"Video #1",
   "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
   "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
   "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
   "length":71517,
   "uploaderId":3511,
   "orderId":1008225
}

```
</details>

<details><summary>Response</summary>

```json
{
   "id":594178,
   "title":"Video #1",
   "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
   "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
   "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
   "length":71517,
   "lastViewedDate":null,
   "playedDuration":null,
   "uploaderId":3511,
   "orderId":1008225
}
```
</details>

# Update Video

Update a video given the passed request
```
PUT /api/v2/{accountId}/video/{id}
```
<details><summary>Request</summary>

```json
{
   "title":"Video #1",
   "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
   "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
   "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
   "length":71517,
   "lastViewedDate":1550694192,
   "playedDuration":71517,
   "uploaderId":3511,
   "orderId":1008225
}

```
</details>

<details><summary>Response</summary>

```json
{
   "id":594178,
   "title":"Video #1",
   "description":"The technician was able to get to the root cause of your concerns. Please check out the video at the link included, and then call me at your convenience to discuss. Robert.",
   "url":"https://tce-in.s3.amazonaws.com/1d7bb67ee34f7578aae8f58625903be4.mp4",
   "thumbnail":"http://dev.truvideo.com/api/v1/files/7ad5799c-968e-4698-bf62-fb9b765d858d.jpg",
   "length":71517,
   "lastViewedDate":1550694192,
   "playedDuration":71517,
   "uploaderId":3511,
   "orderId":1008225
}
```
</details>
