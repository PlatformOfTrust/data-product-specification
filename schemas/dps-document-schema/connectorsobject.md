# ConnectorsObject

The connectors object describes the needed connector component details.

| Field Name | Type | Description |
| :--- | :---: | :--- |
| connectorId | `string` | **Required** Global Unique Identitifer within platform |
| connectorUrl | `uri` | **Required** Location of the connector API endpoint |

**Example:**

```text
{
   "connectors":{
      "connector": {
        "connectorId": "31b5b971-dc50-4c9c-992a-57c0bf016186",
        "connectorUrl": "https..."
      }
   }
}
```

