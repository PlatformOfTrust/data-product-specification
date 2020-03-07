# Data Product Mockup



{% hint style="warning" %}
In Product API implementation it might be a good idea to parametrize the amount of meta data details retrieved for a product and product list. For example "details=\[minimum, all\]". 

This would offer flexibility in limiting the amount of data in cases where just the basic product meta data information is needed. 
{% endhint %}

### Data Product Meta Information

```text

{
  "DataProduct": {
    "@type": "Product",
    "idName": "string", (can contain weird characters and make it hard to use as identifier)
    "idSystem": PoT generated unique id (pick some hashing algorithm)
    "description": "long text",
    "lifecycleStatus: "[draft, development, testing, ready to publish, published, sunset, retired]",
    "version": 1,
    "logo": uri, 
    "images": [
        "https://example.com/photos/1x1/photo.jpg",
        "https://example.com/photos/4x3/photo.jpg",
        "https://example.com/photos/16x9/photo.jpg"
       ],
    "visibility": "[private, organisation, public]",
    "availability" {
      "Continents": "[Europe, Asia, Africa, Oceania, North America, South America, Global]"
      "Countries": "[FI, SE]" // country codes
    },
    "validFrom": data time, (can be empty)
    "validTo": date time, (can be empty),
    "createdAt": datetime,
    "updatedAt": datetime,
    "keywords": "key, word",
    "aggregateRating": {
        "@type": "AggregateRating",
        "ratingValue": "4.4",
        "reviewCount": "89"
      },
    
    "trustIndexValue": string? // Vesa knows about this. 
    "Owner": {
      "orgName": string,
      "orgUri": uri,
      "orgId": string (coming from Platform of Trust),
      "image": uri (logo)
       
      ...
    },
    "Pricing": {
      "currency": "according to some internal standard, one value",
      "PricePlan" {
        "name": "string",
        "description": string,
        "planType": "[subscription, transaction, oneoff]"
        "unitPrice":integer (for one call)
        "callLimit": integer (cap for transaction and oneoff API calls)
        "unitPriceAdditional": integer (price for calls above callLimit)
        "limitPeriod": "[hour, day, week, month, year]" 
        "periodDataCap": {
          "unit": "[GB]",
          "value": integer
        }   
        ...
      }, 
      "PricePlan" {
        "name": "string", 
        "description": string,
        "type": "[subscription, transaction, oneoff]" 
        ...
      }
    },
    "Infrastructure": { 
      "connectors: {
        "connector: {
          "monitoring": status.oftrust.net,
          "name": string,
          "version: integer,
          "uri": uri, 
          "payloadOptions: {
            "currenValues": {
              "parameters" : {
                "startDate" : datetime,
                "endDate" : datetime, 
                "measurements" : "[co2, noise, humid, occupancy, lights, temperature]", (should be defined in connector metadata)
                "limit": integer (default value 500)
                "offset":  
              }
            },
            "historyValues: {},
            "predictionValues": {}
          }
        }, 
        "connector: {
          "monitoring": status.oftrust.net,
          "name": string,
          "version: integer,
          "uri": uri
        }
      }
    },
    "Conditions": {
      "terms": uri,
      "dataLicense":"license",
      "SLA": {
        "objective": {
          "period": "[daily, weekly, monthly]",
          "responseTimeMs": integer, // example 250
          "availability":"[90%, 95%, 97.5%, 98%, 99%, 99.9%, 99.99%]
      }
    },
    "Support": {
      "contact": {
        "hours: "string"
        "phone": string,
        "email": email,
      },
      "online": {
        "stackoverflow":"uri",
        "twitter": uri,
        "chat": uri,
        "ticketSystem": uri
      }
    }
  }
}

```

* * 
### Data Product Payload responses

Data Product payload can have multiple slightly differing payloads. The structure of the schema is otherwise the same, but the `group` element contents and amount depends of the data product decisions made by data product owner. Possible payload options are:

* Current values
* History values
* Prediction values

#### History  values example

In this example data product payload contains historical values of two measurements: CO2 and humidity. 

```text
{
  "DataProductPayload": {
  "@context": "<context url>",
  "idName": string,  // data product name
  "startDate":"date time", 
  "endDate": "date time",
  "signature": {
    "type": "<signature type>",
    "created": "<RFC3339>",
    "creator": "<public key URL>",
    "signatureValue": "..."
  }
  "group" {
      "payloadName": "co2",
      "unit": something, 
      "values": {
          "value": {
              "deviceId:"",
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "deviceId:"",
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "deviceId:"",
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
              "deviceId:"",
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "deviceId:"",
              "dateTime":"jotain", 
              "value": value, 
          },
          "value": {
              "deviceId:"",
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

