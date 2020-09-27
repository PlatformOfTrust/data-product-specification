# PricePlan

PricePlan covers properties that describe pricing. Price related properties include rate, unit and currency. Taxation properties cover applicable VAT percentage and whether or not, tax is included in price. PricePlan also describes what are the possible mechanisms to buy the product – mainly if it is based on transaction or subscription, or if it is a combination of them. Note that one product can have multiple PricePlan options, for example based on customer segmenting profile or area policies.

Supported types of plans are:

| Name | Description |
| :--- | :--- |
| **Free** | Free data  and should not have price other than 0. Free data can be integrated with in-house or private data and this integration could become valuable. |
| **Pay-per-use** | aka usage based pricing, usage based prices correspond to the human rationality that each single unit of a commodity raises the total amount of money to pay for.  |
| **Package pricing** | Package pricing refers to a pricing model that offers a customer a certain amount of data or API calls for a fixed fee. In this context amount of data is data cap which might be attached to plan. API calls is relevant if the product is request-response type. On subscription product this does not make sens. Use Subsription instead |
| **Subscription** | aka The flat fee tariff is one of the simplest pricing models with minimal transaction costs. It is based on time as the only parameter. Suppliers could combine a flat fee tariff with flexibility by offering short term contracts.  |
| **Two-part tariff** | Customers pay a fixed basic fee and on top of that an additional ’fee per unit consumed’. |
| **Freemium** | The idea is to let users join and use basic services for free and charge them for \(premium\) services that provide additional value to customers. The payment model for additional services can take any of the forms described above. |

* Free
* Usage based
* Package pricing
* Flat fee tariff
* Two-part tariff
* Freemium
* Subscription

| Property Category | Property | Type | Label | Description |
| :--- | :--- | :--- | :--- | :--- |
| identifier | name | string | Name | Name of the PricePlan. |
| financial | currency | string | Currency | Currency used for rate. |
| physical | unit | string | Unit | Unit used \(Defines unit which is used\). |
| physical | unitGroup | string | Unit group | Unit group name/definition. |
| financial | vatIncluded | boolean | VAT included in rate | Information if VAT is included in the rate \(price per unit\). |
| financial | vatPercentage | integer | VAT percentage | Percentage value used for VAT taxation. |

### Examples



