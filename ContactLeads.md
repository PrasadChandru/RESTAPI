## Contact Leads [/contact-Leads]
Contact Leads endpoint allows to generates a lead id after saving the details in DB by getting the customer query and process furthur on the query to resolve it.

### contact-Leads
Contact Leads as a resource represents following information

| Property | Type | As request | As response | Description |
| :-------------------- | :---------- | :-------------------- | :-------------------- | :------------------------------------------------------------ |
| id |	String | Not required | Returned always | It helps to identify customer resource. Value is lead id number. |
| title | String | Mandatory | Returned always | It helps to identify customer title value. |
| firstName |String  | Mandatory | Returned always | It helps to identify customer first name value. |
| lastName | String  | Mandatory | Returned always | It helps to identify customer last name value. |
| businessName | String | Mandatory | Returned always | It helps to identify customer business name value. |
| contractAccount | String | Optional | Returned always | It helps to identify customer Contract account number value. |
| emailAddress | String | Mandatory | Returned always | It helps to identify customer email value. |
| phoneNumber | String | Mandatory | Returned always | It helps to identify customer phone number value. |
| address | Object | Mandatory | Returned always | It helps to identify customer address value. |
| query | String | Mandatory | Returned always | It helps to identify customer query value. |
| queryCategory | String | Mandatory | Returned always | It helps to identify customer queryCategory value. |
| queryOption | String | Mandatory | Returned always | It helps to identify queryOptionSelect value. |


### Use cases

## Create a Contact Leads

## Headers
	POST /contactLeads
        cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526
			
## Request

```json
            {
              "contactLeads": {
                "title": "Mr",
                "firstName": "Edwards",
                "lastName": "Church",
                "businessName": "Centrica",
		"contractAccount": "600000329",
                "emailAddress": "britishgas@bggas.co.uk",
                "phoneNumber": {
                      "number": "07404669698",
                      "type": null
                    },
		"address":{ 
			"countryCode": "GB",
 +			"regionCode": "DBY",
 +			"streetPostalCode": "DE21 2DF",
 +			"cityName": "DERBY",
 +			"streetName": "Bishops Drive",
 +			"street2": "",
 +			"street3": "",
 +			"street4": "",
 +			"houseID": "378",
 +			"buildingID": "",
 +			"pOBoxNumber": "",
 +			"pOBoxPostCode": ""
		   },
                "query": "regarding meter select",
                "queryCategory": "My meter reading",
                "queryOption": "Meter reading enquiry"
              },
              "meta": {}
            }
```

## Response 200 (contact-Leads/json)

```json
            {
              "status": "SUCCESS",
              "data": {
                "contactLeads": {
                  "id": "567890329",
                  "title": "Mr",
                "firstName": "Edwards",
                "lastName": "Church",
                "businessName": "Centrica",
		"contractAccount": "600000329",
                "emailAddress": "britishgas@bggas.co.uk",
                "phoneNumber": {
                      "number": "07404669698",
                      "type": null
                    },
		"address":{ 
			"countryCode": "GB",
 +			"regionCode": "DBY",
 +			"streetPostalCode": "DE21 2DF",
 +			"cityName": "DERBY",
 +			"streetName": "Bishops Drive",
 +			"street2": "",
 +			"street3": "",
 +			"street4": "",
 +			"houseID": "378",
 +			"buildingID": "",
 +			"pOBoxNumber": "",
 +			"pOBoxPostCode": ""
		   },
                "query": "regarding meter select",
                "queryCategory": "My meter reading",
                "queryOption": "Meter reading enquiry"
                }
              },
              "errors": [],
              "meta": {}
            }
```

## Request - Customer not authenticated

 ### Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526

### Response 401 (contact-Leads/json)

```json
            {
                "status": "FAIL",
                "data": {},
                "errors": [
                    {
                        "code": "authorize",
                        "message": "access_denied"
                    }
                ],
                "meta": {}
            }
```

## Request - Input Validations

### Headers
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526

## Response 400 (contact-Leads/json)

```json
            {
                "status": "FAIL",
                "data": {},
                "errors": [
                    {
                        "code": "account",
                        "message": "error.client.account.invalid"
                    }
                ],
                "meta": {}
            }
```		

## Request - Error from DB

## Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526
	    
## Response 500 (contact-Leads/json)

```json

  {
	"status": "ERROR",
	"data": {},
	"errors": [{
		"code": "system",
		"message": "error.system.unexpected.error"
	}],
	"meta": {}
}

```
