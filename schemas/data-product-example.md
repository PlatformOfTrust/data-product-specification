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
      "currency": "according to some internal standard, one value",
      "PricePlan" {
        "name": "string",   
        ...
      }, 
      "PricePlan" {
        "name": "string", 
        ...
      }
    },
    "Infrastructure": {
      "monitoring": status.oftrust.net, 
      "connectors: {
        "connector: {
          "name": string,
          "version: integer,
          "uri": uri, 
          "payloadOptions: {
            "currenValues": {
              "parameters" : {
                "startDate" : "Value",
                "endDate" : "Value", 
                "measurements" : "[co2, noise, humid, occupancy, lights, temperature]", 
              }
            },
            "historyValues: {},
            "predictionValues": {}
          }
        }, 
        "connector: {
          "name": string,
          "version: interger,
          "uri": uri
        }
      }
    },
    "Conditions": {
      "terms": "uri",
      "dataLicense":"license",
      "payloadOptions: {
          "currenValues": {
            "parameters" : {
              "startDate" : "Value",
              "endDate" : "Value", 
              "measurements" : "[co2, noise, humid, occupancy, lights, temperature]", 
          }
          "historyValues: {},
          "predictionValues": {}
        }
      ...
    }
  }
}

```

* 
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

