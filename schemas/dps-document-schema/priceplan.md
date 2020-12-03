# PricePlan

PricePlan covers properties that describe pricing. Price related properties include rate, unit and currency. Taxation properties cover applicable VAT percentage and whether or not, tax is included in price. PricePlan also describes what are the possible mechanisms to buy the product – mainly if it is based on transaction or subscription, or if it is a combination of them. Note that one product can have multiple PricePlan options, for example based on customer segmenting profile or area policies.

Supported types of plans are:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Free</b>
      </td>
      <td style="text-align:left">Free data and should not have price other than 0. Free data can be integrated
        with in-house or private data and this integration could become valuable.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Pay-per-use</b>
      </td>
      <td style="text-align:left">aka usage based pricing, usage based prices correspond to the human rationality
        that each single unit of a commodity raises the total amount of money to
        pay for.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Package</b>
      </td>
      <td style="text-align:left">
        <p>Package pricing refers to a pricing model that offers a customer a certain
          amount of data or API calls for a fixed fee and pay fee per unit for exceeding
          calls.</p>
        <p></p>
        <p>In this context amount of data is data cap which might be attached to
          plan. API calls is relevant if the product is request-response type. On
          subscription product this does not make sense.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Subscription</b>
      </td>
      <td style="text-align:left">aka The flat fee tariff is one of the simplest pricing models with minimal
        transaction costs. It is based on time as the only parameter. Suppliers
        could combine a flat fee tariff with flexibility by offering short term
        contracts.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Freemium</b>
      </td>
      <td style="text-align:left">The idea is to let users join and use basic services for free and charge
        them for (premium) services that provide additional value to customers.
        The payment model for additional services can take any of the forms described
        above.</td>
    </tr>
  </tbody>
</table>

### Schema elements

| Property Category | Property | Type | Label | Description |
| :--- | :--- | :--- | :--- | :--- |
| identifier | name | string | Name | Name of the PricePlan. |
| financial | currency | string | Currency | Currency used for rate. |
| physical | unit | string | Unit | Unit used \(Defines unit which is used\). |
| physical | unitGroup | string | Unit group | Unit group name/definition. |
| physical | quantity | integer | Quantity | |
| financial | vatIncluded | boolean | VAT included in rate | Information if VAT is included in the rate \(price per unit\). |
| financial | vatPercentage | integer | VAT percentage | Percentage value used for VAT taxation. |
| financial | rate | string | Rate | |

### Examples

```javascript
{
   "name":"FREE",
   "unitGroup":"Transaction",
   "unit":"Transaction",
   "rate":0
}
```

```javascript
[
   {
      "name":"Premium Package",
      "currency":"EUR",
      "unitGroup":"Transaction",
      "unit":"Transaction",
      "quantity":100000,
      "rule":{
         "maxQuantity":100000
      },
      "rate":100
   },
   {
      "name":"Extra Requests",
      "currency":"EUR",
      "unitGroup":"Transaction",
      "unit":"Transaction",
      "quantity":1,
      "rule":{
         "minQuantity":100001
      },
      "rate":0.5
   }
]
```

```javascript
{
   "name":"Premium subscription 1 year",
   "currency":"EUR",
   "unitGroup":"Duration",
   "unit":"year",
   "quantity":1,
   "rate":1000
}
```

```javascript
{
   "name":"Pay-Per-Use Standard",
   "currency":"EUR",
   "unitGroup":"Transaction",
   "unit":"Transaction",
   "rate":1
}
```