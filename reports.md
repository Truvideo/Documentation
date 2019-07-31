#### Notes: 
1- For all requests the {accountId} path parameter will be present.   
## Export Dealer Bible CSVs

Looks for orders by a time-range and the provided Dealers, then it exports them as CSVs in the configured SFTP Server. All the configurations of the server are looked by Dealer, and if not exists the Default configurations for Truvideo SFTP Servers and provided.
The report definition is the report type that will be in the CSV (headers).
```
POST /api/v2/{{accountId}}/reports/export/dealer-bible
```

<details><summary>Request</summary>

```json
{
	"dateFrom": 1546373480000, 
	"dateTo": 1562616680000,
	"definition": "DEFAULT",
	"dealers": [41]
}
```
</details>

## Import Authenticom CSVs

Looks for un-processed CSVs in Authenticom's FTP Server and process them, creating/updating the contained orders. 
```
POST /api/v2/{{accountId}}/reports/import/authenticom
```
Empty request and response body.