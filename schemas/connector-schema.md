# Connector Schema

Connector schema defined the meta data for connector component. 

```text
{
  "Connector": {
    "idName": "string", (can contain weird characters and make it hard to use as identifier)
    "idSystem": PoT generated,
    "datasourcesystem": "string" // name of the data source system
    "description": "long text",
    "lifecycleStatus: "[draft, development, testing, ready to publish, published, sunset, retired]",
    "version": 1,
    "image": URI,
    "uri": uri, 
    "visibility": "[private, organisation, public]",
    "createdAt": datetime,
    "updatedAt": datetime,
    "dataproducts": [co2, humidity, temperature,....],
    "CreatedBy": {
      "organisation:" {
        "contributionType": "[creator, modifier]",
        "orgName": string,
        "orgUri": uri,
        "orgId": string (coming from Platform of Trust),
        "image": uri (logo)
      },
      "organisation:" {
        "contributionType": "[creator, modifier]",
        "orgName": string,
        "orgUri": uri,
        "orgId": string (coming from Platform of Trust),
        "image": uri (logo)
      }
      ...
    }
  }
  
}
```

