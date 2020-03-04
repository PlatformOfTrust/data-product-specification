# Data Product example

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
          "versio: interger,
          "uri": uri
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
      "dataLicense:"
      ...
    }
  }
}

```

