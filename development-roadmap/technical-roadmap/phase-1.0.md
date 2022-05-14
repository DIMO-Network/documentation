---
description: 'Phase 1.0: Centralized data collection and decentralized data storage'
---

# Phase 1.0

![](<../../.gitbook/assets/phase 1.png>)

\~1.3 million Tesla vehicles and 15 million more cars from other Auto Manufacturers have some form of open API. Due to the cost of sending data over the air, this provides a lower quantity/quality of data, but it is easy to integrate at scale and will allow DIMO to build out polling, storage, and vehicle ID protocol.

During onboarding, the user will provide login credentials that grant DIMO access to collect certain vehicle data by calling an OEM API. A user can then store this information locally, or delegate permission for DIMO to store in an IPFS cluster or Arweave.

Security In the case of existing data provided via API/MQTT/Kafka from OEM APIs, we will leverage DNS and Certificates Trust Chain to validate the data source.

The following smart contracts will be deployed to testnet during Phase 1.0:

| <p><span data-gb-custom-inline data-tag="emoji" data-code="1fa99">🪙</span></p><p>$DIMO Token Issuance</p> | Controls issuance of newly minted $DIMO, including dTeams budgets, demand signal for data provider earnings, and other DAO-directed programs. |            [BAT](https://basicattentiontoken.org/)            |
| :--------------------------------------------------------------------------------------------------------: | --------------------------------------------------------------------------------------------------------------------------------------------- | :-----------------------------------------------------------: |
|                                      <p>🚰</p><p>Live Data Access</p>                                      | Allows user to whitelist entities that can read streaming data from their connected devices.                                                  |              [Streamr](https://streamr.network/)              |
|    <p><span data-gb-custom-inline data-tag="emoji" data-code="1f3db">🏛</span></p><p>DAO Governance</p>    | Controls voting and decision allocation within the DIMO protocol.                                                                             | [Compound Governor](https://compound.finance/docs/governance) |
