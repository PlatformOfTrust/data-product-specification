# Data Product Schema

A data product consists of five different entities: product, service, price plan, condition and quality. The properties that belong to them are described in more detail in each of the sections.

Below is the example of DataProduct. Entitites definitions can be found in respective subpages.

```json
{
   "condition": {
      "name":"Reselling limitation",
      "descriptionGeneral": "Information cannot be sold further.  Only to be used within buying organization",
      "categorizationLocal": "usage",
      "categorizationPoT": "dataProduct"
   },
   "priceplan": {
   		"name":"Organization contact information - Finland",
   		"currency": "euro",
   		"unit": "monthly, quantity",
   		"unitGroup": "subscription, transaction",
   		"vatincluded": "",
   		"vatPercentge": ""
   },
   "quality": {
   		"name":"Information updating",
   		"categorizationLocal": "Update frequancy",
   		"categorizationPoT": "dataProduct",
   		"descriptionGeneral": "Information is updated once per day"
   },
   "service": {
   		"name":"Phone support hours",
   		"descriptionGeneral": "Support is available between 08-16 weekdays.",
   		"categorizationLocal": "Support",
   		"categorizationPoT": "dataProduct"
   },
   "product": {
   		"categorizationPoT": "dataProduct",
   		"descriptionGeneral": "xxxxxxxxxxx",
   		"name": "Organization contact information",
   		"version": "1.0",
   		"visibility": "organisation, public",
   		"validFrom": "2020-01-01",
   		"validTo": "2020-12-31"
   	}
}
```