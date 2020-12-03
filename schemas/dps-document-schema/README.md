# Data Product Schema

Below is the example of DataProduct. Entitites definitions can be found in respective subpages.

```javascript
{
   "name":"Product catalog",
   "categorizationPoT":"dataProduct",
   "descriptionGeneral":"Product catalogs published by standardization organizations.",
   "rating":4.7,
   "visibility":"organisation, public",
   "validFrom":"2020-01-01",
   "validTo":"2020-12-31",
   "status":[
      {
         "name":"Published"
      },
      {
         "name":"Maintenance scheduled",
         "decriptionGeneral":"DataProduct Service Update on Wednesday April 18 at 20:00 UTC. Expected duration 2 hours."
      }
   ],
   "streamType":[
      "current",
      "history"
   ],
   "monitoring":{
      "url":"https://status.uptimerobot.com/"
   },
   "ontology":{
      "harmonized":true,
      "version":"2.0",
      "versionHistory":[
         "1.2",
         "2.0"
      ],
      "requestContext":"https://standards.oftrust.net/v2/Context/DataProductParameters/ProductCatalog/",
      "responseContext":"https://standards.oftrust.net/v2/Context/DataProductOutput/ProductCatalog/"
   },
   "condition":[
      {
         "name":"Reselling limitation",
         "descriptionGeneral":"Information cannot be sold further. Only to be used within buying organization.",
         "categorizationLocal":"usage",
         "categorizationPoT":"only for internal use"
      }
   ],
   "priceplan":[
      {
         "name":"Premium subscription 1 year",
         "currency":"EUR",
         "unitGroup":"Duration",
         "unit":"year",
         "quantity":1,
         "rate":1000
      },
      [
         {
            "name":"Premium Package",
            "currency":"EUR",
            "unitGroup":"Transaction",
            "unit":"Transaction",
            "quantity":100000,
            "rule":{
               "maxQuantity":100000
            },
            "rate":100
         },
         {
            "name":"Extra Requests",
            "currency":"EUR",
            "unitGroup":"Transaction",
            "unit":"Transaction",
            "quantity":1,
            "rule":{
               "minQuantity":100001
            },
            "rate":0.5
         }
      ]
   ],
   "quality":[
      {
         "name":"Information updating",
         "categorizationLocal":"Update frequancy",
         "categorizationPoT":"dataProduct",
         "descriptionGeneral":"Information is updated once per day."
      },
      {
         "name":"Uptime",
         "value":"99%"
      },
      {
         "name":"Response time",
         "value":"400 ms"
      }
   ],
   "service":[
      {
         "name":"Phone support hours",
         "descriptionGeneral":"Support is available between 08-16 weekdays.",
         "categorizationLocal":"Support",
         "categorizationPoT":"dataProduct"
      }
   ],
   "connector":[
      {
         "name":"Electrical devices catalog",
         "descriptionGeneral":"Catalog of electrical devices.",
         "version":"2.0",
         "monitoring":{
            "url":"https://status.uptimerobot.com/"
         },
         "quality":[
            {
               "name":"Uptime",
               "value":"99%"
            },
            {
               "name":"Response time",
               "value":"400 ms"
            }
         ],
         "url":"https://connector.com/api/methodname",
         "ontology":{
            "harmonized":true,
            "version":"2.0",
            "versionHistory":[
               "1.2",
               "2.0"
            ],
            "requestContext":"https://standards.oftrust.net/v2/Context/DataProductParameters/ProductCatalog/",
            "responseContext":"https://standards.oftrust.net/v2/Context/DataProductOutput/ProductCatalog/"
         }
      },
      {
         "name":"Furniture  catalog",
         "description":"Catalog of furniture.",
         "version":"3.0",
         "monitoring":{
            "url":"https://status.uptimerobot.com/"
         },
         "quality":[
            {
               "name":"Uptime",
               "value":"99%"
            },
            {
               "name":"Response time",
               "value":"400 ms"
            }
         ],
         "url":"https://connector.com/api/methodname",
         "ontology":{
            "harmonized":false
         }
      }
   ]
}
```

| Property Category | Property | Type | Label | Description |
| :--- | :--- | :--- | :--- | :--- |
| description | condition | Condition | Condition | Conditions associated with DataProduct. |
| description | priceplan | PricePlan | PricePlan | PricePlans associated with DataProduct. |
| description | quality | Quality | Quality | Quality associated with DataProduct. |
| description | service | Service | Service | Service associated with DataProduct. |
| description | connector | Connector | Connector | Connector implementations of DataProduct. |
| categorization | categorizationETIM | string | ETIM class name | Product category name based on ETIM standard \(\(European Technical Information Model\). |
| categorization | categorizationPoT | valueset | PoT category | Categorization class name in PoT standard. |
| description | additionalInformation | string | Additional information | Additional information. |
| description | descriptionGeneral | string | Description | Description. |
| description | imageUrl | string | Product image | Link to product image. |
| financial | priceCurrent | decimal | Estimated price | Estimated value of the current price. |
| financial | pricePurchase | decimal | Purchase price | Purchase price. |
| financial | priceSell | decimal | Sales price | Sales price. |
| identifier | codeProduct | string | Product code | Unique product code given by manufacturer. |
| identifier | ean | string | EAN code | EAN standard based identifier. |
| identifier | gTIN | string | GTIN code | GTIN standard based identifier. |
| identifier | groupCode | string | Product group code | Unique product group code given by manufacturer. |
| identifier | groupName | string | Product group name | Unique product group name given by manufacturer. |
| identifier | id | string |  |  |
| identifier | name | string | Name | Name. |
| identifier | url | string | URL address | URL address. |
| identifier | logo | string | | |
| lifeCycle | status | string | Life-cycle status | Life-cycle status. |
| lifeCycle | version | string | Version name | Version name. |
| metadata | createdAt | dateTime | Creation time | Time when the data is created. |
| metadata | createdBy | string | Creator | Creator of and identity. |
| metadata | updatedAt | dateTime | Update time | Time when the data is updated. |
| metadata | updatedBy | string | Updater | Updater of an identity. |
| other | visibility | valueset | Product visibility | Product visibility restriction defined by PoT. |
| time | validFrom | dateTime | Validity period start time | Validity period start time. |
| time | validTo | dateTime | Validity period end time | Validity period end time. |

Value sets

| Property Category | Property | List of values |
| :--- | :--- | :--- |
| lifeCycle | status | planned, in development, ready for publish, active/published, supported, not in support, retired, replaced |