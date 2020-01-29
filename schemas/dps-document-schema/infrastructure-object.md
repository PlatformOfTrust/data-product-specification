# InfrastructureObject

The infrastructure object describes the operational tooling to use in the service execution.

| Field Name | Type | Description |
| :--- | :---: | :--- |
| supervisor | `uri` | **Required** Location of the SLA Check service accordingly to the Basic SLA Management Service spec. |
| monitor | `uri` | **Required** Location of the SLA Metrics endpoint accordingly to the Basic SLA Management Service spec. |
| connectors | `object` | **Required** Connector component. |
| consentManagement | `object` | **Required** Consent management. |

**Example:**

```text
{
   "infrastructure":{
      "supervisor": "http://supervisor.sla4oai.governify.io/v1/",
      "monitor": "http://platformoftrust.statuspage.io"
      "connectors: {
      ...
      }
   }
}
```

