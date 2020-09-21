# Price Plan

PricePlan covers properties that describe pricing. Price related properties include rate, unit and currency. Taxation properties cover applicable VAT percentage and whether or not, tax is included in price. PricePlan also describes what are the possible mechanisms to buy the product – mainly if it is based on transaction or subscription, or if it is a combination of them. Note that one product can have multiple PricePlan options, for example based on customer segmenting profile or area policies.

| Property Category | Property | Type | Label | Description |
| :--- | :--- | :--- | :--- | :--- |
| identifier | name | string | Name | Name of the PricePlan. |
| financial | currency | string | Currency | Currency used for rate. |
| physical | unit | string | Unit | Unit used (Defines unit which is used). |
| physical | unitGroup | string | Unit group | Unit group name/definition. |