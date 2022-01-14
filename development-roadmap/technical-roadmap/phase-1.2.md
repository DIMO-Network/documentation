---
description: >-
  Phase 1.2: Functional NFTs, direct OEM integration, and centralized data
  unions
---

# Phase 1.2

![](<../../.gitbook/assets/phase 3.png>)

### Functional NFTs

DIMO will enable ownership of the vehicle through an NFT. The user will be able to interact (unlock/lock/drive), give partial/limited ownership or transfer ownership to other people, effectively delegating control over the car and its connected functionality to the holder in a secure, transparent, and programmable manner.

The following smart contracts will be deployed to during Phase 1.2:

| <p> 🚗 </p><p>Vehicle NFT Ownership</p> | Stores & manages user (wallet) and device relationships, including roles which mediate access to services. | [Unlock Protocol](https://docs.unlock-protocol.com/creators/customizing-the-nft) |
| :-------------------------------------: | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |

### Native OEM Integration

This phase will also enable the removal of plug-in devices from the vehicle and direct integration with the automotive OEMs.

3rd-party plugin devices will be a supported option that provides additional security, redundancy, and functionality - similar to “running your own node” in traditional blockchain networks. This will allow for verified data streams to continue to be collected by fleet operators, insurance companies, and device owners who do not want to rely on OEMs for connectivity.

### Data Union Operators

Any whitelisted operator will be able generate demand signals for data and create products that access and resell data per predefined terms (specifying pricing, revenue splits, permissible uses and more).

They’re responsible for producing datasets that are (1) desired by data consumers, and (2) aligned with the interests of their members (data providers). These operators will need to stake $DIMO in order to earn a whitelist status, which can be slashed and distributed to impacted users if terms of service are violated.

The dataset can be produced in two formats. (1) A stream of live data coming from the user’s vehicles with minimal delay. (2) A specific data set to answer a direct question, such as battery health across different geographic regions.

To complete a transaction from data collection to utilization a variety of parties with different interests and specializations need to interact. Data must make its way from devices to the Data Union(s), then to data consumers and app developers. We’ve established roles and interfaces to remove as much friction as possible throughout the process.&#x20;

### Data Brokers

Most large traditional enterprises interested in this data will not be ready to interact with a decentralized protocol, so we will introduce Data Brokers which will serve as the middle layer between the Data Union(s) and the end customers.&#x20;

In Phase 1.2, DIMO will use Digital Infrastructure Inc to act as a good faith broker to the DAO. This entity will pull all data, normalize it, package it, and sell it in the form of data sets, APIs, and other subscriptions.

This entity would then flow profits back into the DAO treasury.

Data will be available in three formats, and the Data Union Operator can also bundle them into subscription packages that are approved by users:

**🚿Data Streams:** Entire datasets available from the Data Union(s) with parameters set by the consumer such as the number, or type, of devices to include in the data and the refresh period. Typical comparables in the space today use pricing models on a per car per month basis for this type of data.

**📲APIs:** A curated collection of APIs that may provide specific details out of the dataset within the Data Union. DIMO will develop these APIs based on the demand from data consumers. These APIs may be priced on a per call basis or other methods that are common in the industry.

**💾Custom (one-off) Datasets:** A bulk dataset from a specified group of vehicles that have agreed to provide historical access for acceptable use-cases.

### **How is Data Priced?**&#x20;

As is standard in the data industry, prices will eventually adjust based on the amount of data being consumed; and flexibility will be added to the system to accommodate dynamic consumption and pricing arrangements.

In Phase 2 and beyond, there could be any combination of data brokerage options, which will ultimately be mediated and regulated by the DAO. A few examples include:

1. The DAO builds a decentralized data hub and UI that allows end consumers to purchase data directly without a broker, as well as new demand signals for data and connectivity.&#x20;
2. The DAO whitelists multiple data brokers and applications who agree on pricing and other terms; and/or&#x20;
3. The steward entity from Phase 1 continues operating as a non-profit broker, funneling profits back to the DAO (this is the worst and least likely option).

In all three scenarios, brokers and consumers would stake $DIMO that would be slashed in the event they violate the terms and conditions.&#x20;

The size of the required lockup will generally follow a curve based on the amount of data being consumed or subscribed to, as well as the device functionality exposed to the app in question.
