# Data Product example

### Data Product Meta Information

```text

{
  "DataProduct": {
    "idName": "string",
    "description": "31b5b971-dc50-4c9c-992a-57c0bf016186",
    "status: "[draft, development, ready to publish, published, retired]",
    "version": 1,
    "image": URI, 
    "validFrom": data time, 
    "validTo": date time, 
    "Owner": {
      ...
    },
    "Pricing": {
      "PricePlan" {
        "name": "string", 
        "currency": "according to some internal standard, one value", 
        ...
      }, 
      "PricePlan" {
        "name": "string", 
        "currency": "according to some internal standard, one value", 
        ...
      }
    },
    "Infrastructure": {
      "monitoring": uri, 
      "connectors: {
        "connector: {
          "name": string,
          "versio: integer,
          "uri": uri, 
        }, 
        "connector: {
          "name": string,
          "versio: interger,
          "uri": uri
        }
      }
    },
    "Conditions": {
      "terms": "string",
      "dataLicense":"license",
      "payloadOptions: {
          "currenValues": boolean {
            "parameters" : {
              "param-1" : "Value",
              "param-2" : "Value"
          }
          "historyValues: boolean,
          "predictionValues": boolean
        }
      ...
    }
  }
}

```

### Data Product Payload response

```text
{
  "DataProduct": {
  "payloadOption: "currentValues", 
  "values": {
      "name": "jotain";
  }
  
  "links": [
      {
          "rel": "self",
          "href": "http://api.oftrust.net/v1/marketplace/apps?limit=30",
      },
      {
          "rel": "first",
          "href": "http://api.oftrust.net/v1/marketplace/apps?limit=30&from=0",
      },
      {
          "rel": "next",
          "href": "http://api.oftrust.net/v1/marketplace/apps?limit=30&from=30",
      }
  ]
  
  
```

