## ContactLeads [/contactLeads]
ContactLeads takes the query from customer and generates a lead id to proceed furthur on the query to resolve it.

### contactLeads
contactLeads resource information

| Property | Type | As request | As response | Description |

| :-------------------- | :---------- | :-------------------- | :-------------------- | ------------------------------------------------------------ |
|id|	String | Not required | Returned always | Its helps to identify customer resource. Value is combination of lead id and acc.number.|
|title|String | Optional | Returned always | Its helps to identify customer title value.|
|firstName|String  | Optional | Returned always| Its helps to identify customer first name value.|
|surname|String  | Optional | Returned always| Its helps to identify customer sur name value.|
|businessName|String| Optional | Returned always| Its helps to identify customer business name value.|
|accountNumber|String| Optional | Returned always| Its helps to identify customer accountNumber value.|
|emailAddress|String| Optional | Returned always| Its helps to identify customer email value.|
|telephoneNumber|String| Optional | Returned always| Its helps to identify customer phone number value.|
|postcode|String| Optional | Returned always| Its helps to identify customer postcode value.|
|address|String| Optional | Returned always| Its helps to identify customer address value.|
|query|String| Optional | Returned always| Its helps to identify customer query value.|
|queryCategory|String| Optional | Returned always| Its helps to identify customer queryCategory value.|
|queryOptionSelect|String| Optional | Returned always| Its helps to identify queryOptionSelect value.|


### Use cases

### Create an contactLeads [POST /contactLeads]
+ Request

		+ Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526
			
	    + Body

            {
              "contactLeads": {
                "title": "Mr",
                "firstName": "Edwards",
                "surname": "Church",
                "businessName": "Centrica",
				 "accountNumber": "600000329",
                "emailAddress": "britishgas@bggas.co.uk",
                "telephoneNumber": "02071234567",
                "postcode": "le4 5ex",
				 "address": "21 VICTORIA ROAD NORTH LEICESTER LE4 5EX",
                "query": "regarding meter select",
                "queryCategory": "My meter reading",
                "queryOptionSelect": "Meter reading enquiry"
              },
              "meta": {}
            }
+ Response 200 (contactLeads/json)

            {
              "status": "SUCCESS",
              "data": {
                "contactLeads": {
                  "id": "567890329",
                  "title": "Mr",
                "firstName": "Edwards",
                "surname": "Church",
                "businessName": "Centrica",
				 "accountNumber": "600000329",
                "emailAddress": "britishgas@bggas.co.uk",
                "telephoneNumber": "02071234567",
                "postcode": "le4 5ex",
				 "address": "21 VICTORIA ROAD NORTH LEICESTER LE4 5EX",
                "query": "regarding meter select",
                "queryCategory": "My meter reading",
                "queryOptionSelect": "Meter reading enquiry"
                }
              },
              "errors": [],
              "meta": {}
            }
			
+ Request 'Customer not authenticated'

    + Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526

     + Response 401 (contactLeads/json)

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

+ Request 'Input Validations'

    + Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526

+ Response 400 (contactLeads/json)

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
			
+ Request 'Error from DB'

    + Headers

            Authorization: Bearer {accesstoken}
            cid: 05e230bf-a9cf-4b31-bc54-d3a995f62526

+ Response 500 (application/json)

        {
            "status": "ERROR",
            "data": {},
            "errors": [
                {
                    "code": "system",
                    "message": "error.system.unexpected.error"
                }
            ],
            "meta": {}
        }
