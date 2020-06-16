---
description: 'version: draft'
---

# Data Product Specification Summary \(DRAFT\)

## Introduction

Platform of Trust has taken the initiative to formulate Data Product Specification (DPS) to enhance the open data movement. We are formulating the commercial aspects related to monetizing data in a form of data products. The goal is to enable data rights holders to commercialize their data in order to accelerate the emerging data economy.

An underlying enabler is the universal information model (Platform of Trust Ontology) which allows data to be harmonized across business domains. Once data is harmonized it becomes critical that commercialization of the data is easy and transparent. Commercial transactions should be controlled and monitored so that trust between data publishers and customers can be achieved.

Platform of Trust is enabling an ecosystem where all aspects of data commercialization and transactions can be achieved in a controllable and trustworthy manner.

## Main components of Platform of Trust

* Platform of Trust Ontology
* API (Connector) layer
* Identity Network
* Data Product Management layer
* Data Product Specification

## Main layers of Data Product Specification

Data Product Specification has three main layers. 
* Data Product Model 
* Data Product Structure 
* Payload model

## Key entities of Data Product Model

The main principle of modeling entities and properties related to a data product is to enable flexible and extendable creation of data products. Some data products have simple commercial terms while other’s terms can be complex. Platform of Trust model provides easy creation of simple data products but sets no limits for including additional product related information.

**Product** covers properties that describe commercial information about the product such as commercial names, product codes, versions and life-cycle status.

**PricePlan** covers properties that describe pricing. Price related properties include rate, unit and currency. Taxation properties cover applicable VAT percentage and whether or not, tax is included in price. PricePlan also describes what are the possible mechanisms to buy the product – mainly if it is based on transaction or subscription, or if it is a combination of them. Note that one product can have multiple PricePlan options, for example based on customer segmenting profile or area policies.

**Condition** covers properties related product limitations which describe how a product can be used. For example, whether a product can be resold further, or for what purposes the product can be used, and by whom. Conditions can be divided in non-negotiable product conditions, and negotiable contract conditions. It is up to a data publisher to decide how the conditions are negotiated, and which of them negotiable. It is possible to set all contract conditions as non-negotiable, that means the product is offered in “take it or leave it” principle.

**Services** covers properties which describe service processes that are available for the product.  They can be related to product design, production, selling/buying, delivery, support and invoicing.

**Quality** covers properties which describe qualitative parameters related to either product or services. If qualitative parameters can be monitored, it is possible to set target value ranges for the quality properties, and SLA clauses can be formulated into contracts between a data publisher and a customer. Product can contain these SLA options (product conditions) or they can be agreed in a contract between a publisher and a customer. The possible actions caused by breaching SLA clauses are also agreed in the contract. It is possible for a seller to define them as part of product conditions, and then they are non-negotiable on contract level.

**Contract** gathers together in one document all negotiated and non-negotiable information of a data product. A contract is formed when a data product customer purchases a product. A data publisher may set terms and conditions of a contract to be negotiable or non-negotiable. A contract defines all parties and their roles related to a data product. The parties must include at least a data publisher and a data product customer. If there are any other relevant parties, they must be defined. The permissions needed to access data are derived from roles and conditions of a contract. Other information defined in a contract is a term, limitations of use and payment related information, as well as what how to proceed if a party wants to stop using a data product.

Due to nature of data products, Platform of Trust is suggesting a data product license (DPL) as a default contract for data product market. In order to be compatible with systems relying on automation, a DPL should be a smart contract that means a computer program or a transaction protocol, which is intended to automatically execute, control or document legally relevant events and actions according to the terms of a DPL.

