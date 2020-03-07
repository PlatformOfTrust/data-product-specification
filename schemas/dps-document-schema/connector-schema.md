# Connector Schema

Connector schema defined the meta data for connector component. 

```text
{
  "Connector": {
    "idName": "string", (can contain weird characters and make it hard to use as identifier)
    "idSystem": PoT generated,
    "description": "long text",
    "lifecycleStatus: "[draft, development, testing, ready to publish, published, sunset, retired]",
    "version": 1,
    "image": URI,
    "uri": uri, 
    "visibility": "[private, organisation, public]",
    "createdAt": datetime,
    "updatedAt": datetime,
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

