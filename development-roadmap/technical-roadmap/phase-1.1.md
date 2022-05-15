---
description: 'Phase 1.1: Decentralized data collection and identity'
---

# Phase 1.1

![](<../../.gitbook/assets/phase 2.png>)

### Decentralized Identification (DID)

Today, Automotive OEMs control the digital identity of a vehicle by issuing a communication certificate signed by the OEM. The vehicle cannot transact on its own and is only allowed to interact through the OEM or with OEM itself. The DMV and your insurance provider also separately store and manage various credentials.

#### Vehicle DID&#x20;

Sybil attacks are not a unique problem to DIMO, but the existing trust models of the automotive industry provide unique tools to validate (1) a car exists and has certain properties, (2) the user has ownership of that car, and (3) it has actually been driven.

![](<../../.gitbook/assets/image (10) (1) (1).png>)

Each device in the DIMO network will have its own DID (Decentralized Identity) which conforms to a [W3C standard](https://www.w3.org/TR/did-core/). Such identity exists without any central authority and is securely and privately linked to other identities (e.g., an owner and authorized drivers). This allows the device to manage its own data and, in the future, transact with other devices.

The cost of the “minting” a device as an on-chain NFT should provide some protection from sybil attacks. Each device DID will reference where the encrypted and signed data is stored. This will provide a future-proof way to address the device as well as integrate with other distributed systems.

#### User DID&#x20;

We will closely monitor and contribute to the anti-sybil and proof of personhood infrastructure that is in development by various web3 companies such as Gitcoin, IDX, BrightID, and others. As the Zero Knowledge Proof and DID space evolves, we will utilize these tools to further decentralize user/device information and improve privacy beyond what is possible today.

### Open Hardware

#### OEM Device #1: DIMO x AutoPi Miner&#x20;

DIMO is seeding an independent hardware ecosystem by partnering with Autopi to produce a plug & play, fully integrated ARM-based open hardware product that can plug into any car made after 1988. This device will communicate with the vehicle message bus, called the CAN-BUS and extract signals information sent by the car, as well as sign it to provide authenticity to the data by signing it using the included Ethereum wallet.

![DIMO x AutoPi co-branded OBDII device and its key features](<../../.gitbook/assets/image (12) (1).png>)

Users will be able to add this hardware to their vehicle as either a primary (and only) data collection option, or layer it onto existing API connectivity options provided by the OEM.

#### Open Hardware Spec

The DIMO DAO will publish a certification process for new hardware devices as additional data markets are created, borrowing from the same model developed [by Helium](https://github.com/helium/HIP/blob/master/0019-third-party-manufacturers.md).

The reference design will be available to any 3rd party hardware device makers who wish to add additional features (like dash cams or other sensors) and/or produce their own devices capable of mining $DIMO by providing data. Existing open-source hardware options like [Comma.Ai](https://comma.ai/compare), [CanServer](http://www.jwardell.com/canserver/), and others will be able to integrate seamlessly with DIMO after a software or firmware update.

#### Establishing Data Privacy & Validity

With DIMO, vehicle owners control connections to their devices in cryptographically secure and anonymized ways. Given that anyone can participate in the DIMO network, data payloads of devices are strongly encrypted using asymmetric key cryptography. Only parties holding an authorized private key can read the data. The key to the data will be held in a smart contract which will define the parties that can access the key and the data. This will guarantee that only the authorized recipients can access the data. Multicast encryption techniques may be used in the future to frequently rotate the keys to the data and selectively block data consumers who are misbehaving.

Additionally, DIMO will prioritize user privacy by utilizing zero-knowledge proofs, separating personally identifiable information wherever possible, and providing users with fine grained opt-in data sharing controls, rather than all-or-nothing or complex opt-out controls, as has become the norm in many web2.0 applications.

#### Anti-Spoofing & Secure Hardware Element

To guarantee the security and authenticity of the device data being sent over the network, the data will be signed by an Ethereum (or similar) wallet using secp256k1 ECDSA signing and verification. The data will be validated on receipt and checked against historical data from the device, and other meta-information contained in the payload.

DIMO will be leveraging a secure element in the hardware used to collect the data directly from vehicles. The TEE environment provided by [modern ARM processors](https://www.arm.com/why-arm/technologies/trustzone-for-cortex-a/tee-reference-documentation) will be used to protect against spoofing and provide a future proof location for executing transactions on the device itself as the vehicle becomes a larger compute platform that can execute Solidity code locally on the device.

### **DIMO Signals**

Building on the work established by projects like [OpenDBC](https://github.com/commaai/opendbc), [Open Vehicle Data Farming](https://docs.google.com/document/d/1i8XxRadq2Bta5hJDSOD4oXO\_q63xtuaE6cxzpSKB7e4/edit?usp=sharing) will add token incentives that supercharge efforts to decode data from cars in a standardized and scalable way.

📟 Odometer: Distance travelled by the vehicle

\#️⃣ VIN (Vehicle ID): Includes attributes, manufacturing location, ownership history

📈 State of Charge: Current % and mileage estimate provided by the OEM

📍 Exact Location: 2 decimal point precision (or greater) lat/long values assigned to a device (this gives > 1.1KM location specificity)

🚨 Fault Codes: [Diagnostic trouble codes](http://www.totalcardiagnostics.com/support/Knowledgebase/Article/View/21/0/genericmanufacturer-obd2-codes-and-their-meanings)

A portion of the rewards for drivers of a make and model that are not yet compatible with DIMO (e.g., their vehicle data is not yet decoded) will be programmatically siphoned into bounty pools. Data engineers will be able to fulfill these bounties and earn the pool of $DIMO once successful. After this is complete, drivers will earn full rewards. This creates a market driven means for DIMO to integrate new vehicle types.

As demand for vehicle data and connectivity increases, the rewards calculation will be first supplemented by and then fully supplanted by demand-side signals and economic flow.
