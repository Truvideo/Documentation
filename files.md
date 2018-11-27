# Get File Metadata

Returns the file metadata for the passed file uuid.
```
GET /files/metadata/{uuid}
```
<details><summary>Response</summary>

```json
{
    "uuid": "ac1cd205-709f-40c5-9bd4-ff5acc770704",
    "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
    "name": "JPEG_20181121_092357_894091519.jpg",
    "size": 211390,
    "contentType": "application/octet-stream"
}
```
</details>

# Get Files By Entity

Returns the files associated with the entity type and entity id.
```
GET /files/entity/{entityType}/{entityID}
```
<details><summary>Response</summary>

```json
[
    {
        "metadata": {
            "uuid": "eebd9833-6ab4-439f-b0e7-9fc0b367fc8b",
            "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
            "name": "image.jpg",
            "size": 429364,
            "contentType": "image/jpg"
        },
        "position": 0,
        "properties": {
           
        }
    },
    {
        "metadata": {
            "uuid": "b3d4bce8-d432-4f22-be73-d06337f9f518",
            "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
            "name": "image.jpg",
            "size": 496719,
            "contentType": "image/jpg"
        },
        "position": 1,
        "properties": {
            
        }
    }
]
```
</details>

# Assign Files to an Entity

Associate files to an entity
```
POST /files/entity/{entityType}/{entityID}
```
<details><summary>Request</summary>

```json
[
  {
    "uuid":"03821eb6-f4b8-4608-882c-3eead78e769e",
    "properties":{
    }
  },
  {
    "uuid":"f09ed9e2-f1c7-4338-bc95-ac7d6fad5ee1",
    "properties":{
    }
  },
  {
    "uuid":"85138350-3c32-404e-9740-c5bf0b439f3f",
    "properties":{
    }
  }
]

```
</details>

<details><summary>Response</summary>

```json
[
    {
        "metadata": {
            "uuid": "eebd9833-6ab4-439f-b0e7-9fc0b367fc8b",
            "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
            "name": "image.jpg",
            "size": 429364,
            "contentType": "image/jpg"
        },
        "position": 0,
        "properties": {
           
        }
    },
    {
        "metadata": {
            "uuid": "b3d4bce8-d432-4f22-be73-d06337f9f518",
            "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
            "name": "image.jpg",
            "size": 496719,
            "contentType": "image/jpg"
        },
        "position": 1,
        "properties": {
            
        }
    }
]
```
</details>

# Get File Binary

Returns the file metadata for the passed file uuid.
```
GET /files/{url}
```
<details><summary>Response</summary>

```
Binary Content
```
</details>

# Upload File Binary

Uploads a file (Multipart Request)
```
POST /files
```
<details><summary>Response</summary>

```json
{
    "uuid": "ac1cd205-709f-40c5-9bd4-ff5acc770704",
    "url": "http://dev.truvideo.com/api/v1/files/ac1cd205-709f-40c5-9bd4-ff5acc770704.jpg",
    "name": "JPEG_20181121_092357_894091519.jpg",
    "size": 211390,
    "contentType": "application/octet-stream"
}
```
</details>



