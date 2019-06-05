#### Notes: 
1- For all requests the {accountId} path parameter will be present.   

# Send Email to Support

```
POST /api/v2/{{accountId}}/support/email
```

<details><summary>Request</summary>

```json
{
	"dealerId": "dealerId",
	"dealerName": "dealerName",
	"userId": "userId",
	"appVersion": "1.0",
	"dateTime": "dateTime",
	"phoneId": "phoneId",
	"phoneType": "phoneType",
	"phoneOsVersion": "phoneOsVersion",
	"wifiInternetSettings": "wifiInternetSettings",
	"truVideoServer": "truVideoServer",
	"memoryFree": "memoryFree",
	"storageFree": "storageFree",
	"videoStored": "videoStored",
	"locationServices": "locationServices",
	"location": "location",
	"accessToMicrophone": "accessToMicrophone",
	"notifications": "notifications",
	"autoRotate": "autoRotate",
	"googlePlayAccount": "googlePlayAccount",
	"networkType": "networkType",
	"networkTest": "networkTest",
	"bandwidthTest": "bandwidthTest",
	"videoSettings": "videoSettings",
	"comment": "comment"
}
```
</details>