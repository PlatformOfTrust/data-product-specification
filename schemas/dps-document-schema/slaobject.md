# SlaObject

SLA Object The SLA Object must conform to the following constraints.

| Field Name | Type | Description |
| :--- | :--- | :--- |
| infrastructure | `InfrastructureObject` | **Required** Provides information about tooling used for SLA storage, calculation, governance, etc. |
| pricing | `PricingObject` | **Optional** Global pricing data. |
| metrics | `MetricsObject` | **Required** A list of metrics to use in the context of the SLA. |
| plans | `PlansObject` | **Optional** A set of plans to define different service levels per plan. |
| quotas | `QuotasObject` | **Optional** Global quotas, these are the default quotas, but they could be overridden by each plan later. |
| serviceManagement | `ServiceManagementObject` | **Optional** Effective support of in-scope services is a result of maintaining consistent service levels. |
| visibility | `string` | **Required** Public, private, organisation |
| status | `string` | **Required** idea, draft, testing, staging, production, retired |
| regionsAvailability | `string` | **Required** all, North America, South America, Europe, Asia, Africa |

