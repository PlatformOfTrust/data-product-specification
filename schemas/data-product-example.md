# Data Product example

### Data Product Meta Information

```text

{
  "DataProduct": {
    "idName": "string", (can contain weird characters and make it hard to use as identifier)
    "idSystem": PoT generated unique id (pick some hashing algorithm)
    "description": "long text",
    "status: "[draft, development, ready to publish, published, retired]",
    "version": 1,
    "image": URI, 
    "visibility": "[private, organisation, public]"
    "validFrom": data time, (can be empty)
    "validTo": date time, (can be empty)
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
                "limit": integer (default value 500) 
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
      "SLA": {
      
      }
      
    }
  }
}

```

### Data Product Payload response

```text
{
  "DataProduct": {
  "payloadOption: "historyValues", 
  "startDate":"date time", 
  "endDate": "date time",
  "group" {
      "payloadName": "co2",
      "unit": something, 
      "values": {
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          }
      }
  },
  "group" {
      "payloadName": "humid",
      "unit": something, 
      "values": {
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "dateTime":"jotain", 
              "value": value, 
          }
      }
  },
  
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

