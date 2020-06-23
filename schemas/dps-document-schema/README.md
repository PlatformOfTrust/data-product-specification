# Data Product Schema

| Property Category | Property | Type | Label | Description |
| :--- | :--- | :--- | :--- | :--- |
| categorization | categorizationETIM | string | ETIM class name | Product category name based on ETIM standard ((European Technical Information Model). |
| categorization | categorizationPoT | valueset | PoT category | Categorization class name in PoT standard. |
| description | additionalInformation | string | Additional information | Additional information. |
| description | descriptionGeneral | string | Description | Description. |
| description | imageUrl | string | Product image | Link to product image. |
| identifier | codeProduct | string | Product code | Unique product code given by manufacturer. |
| identifier | groupCode | string | Product group code | Unique product group code given by manufacturer. |
| identifier | groupName | string | Product group name | Unique product group name given by manufacturer. |
| identifier | name | string | Name | Name.
| identifier | url | string | URL address | URL address. |
| lifeCycle | status | string | Life-cycle status | Life-cycle status.
| lifeCycle | version | string | Version name | Version name. |
| metadata | createdAt | dateTime | Creation time | Time when the data is created.
| metadata | createdBy | string | Creator | Creator of and identity. |
| metadata | updatedAt | dateTime | Update time | Time when the data is updated. |
| metadata | updatedBy | string | Updater | Updater of an identity. |
| other | visibility | valueset | Product visibility | Product visibility restriction defined by PoT. |
| time | validFrom | dateTime | Validity period start time | Validity period start time. |
| time | validTo | dateTime | Validity period end time | Validity period end time. |