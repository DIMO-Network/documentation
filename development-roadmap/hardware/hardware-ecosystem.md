# Hardware Ecosystem

### Overview&#x20;

To deliver on the Progressive Decentralization plan for the DIMO project, Digital Infrastructure Inc is exiting the hardware business, and working with AutoPi and the DIMO foundation to establish a process for funding, certifying, and integrating new hardware devices.&#x20;

**Goals**&#x20;

Build a diverse ecosystem of hardware providers (OEMs), retail/distributors, and support channels which give users the best options for taking control of their mobility data, while ensuring support for future DIMO platform features like ADAS (automated driving) and video data collection.   &#x20;

* **🔩 Solve Key hardware manufacturer problems:**     &#x20;
  * 🤖Standardized device management software & APIs
  * 📦Supply chain scale and finance (crypto-enabled preorders)&#x20;
* **🙋‍♀️ Solving Key User Problems**
  * 📈Preorder spots as NFTs (tradeable, arbitrary & standardized terms)&#x20;
  * 📇Certification and Performance Tracking&#x20;
    * Know what you’re getting and when&#x20;
    * Realtime aggregated updates on device-specific performance

The alpha version of the DIMO network software is currently available at app.dimo.zone, and we encourage new vendors to help us develop the software that will become the v1 of the specification and requirements.&#x20;

Future versions of the requirements will be funded by the DIMO foundation and managed by the DIMO Hardware approval team, in close collaboration with other teams responsible for the software roadmap, ecosystem permitting, and community representatives. &#x20;

### Integration Requirements

The following features are required to have a fully DIMO-certified device. Manufacturers can choose to be fully compliant or leave out specific functionality (such as DBC logger configuration) based on their target market and desired featureset.&#x20;

| **Certification**                                  | **Description**                                                                                                                                                                                                                                                                                                                                                                                |
| -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hardware Secure Element**                        | The identity of the device and the vehicle it is connected to is of high importance to the DIMO protocol. In the web3 world, this is known as a “wallet”, but is essentially a private key to identify the device. To limit spoofing, DIMO requires the private keys to be stored inside a hardware secure element.  This key is also used for encrypted, secure transmission of vehicle data. |
| **Implementation of the DIMO streaming interface** | DIMO will provide a specification for how the data should be formatted(schema) and sent to the protocol(delivery). Initially, the data will be sent in compressed json, moving to more efficient binary methods of encoding such as protobuf or avro.                                                                                                                                          |
| **Bluetooth interface**                            | Similar to other IOT devices, DIMO compatible hardware is paired to the user via Bluetooth. This is the initial use case for Bluetooth interface, which will expand in the future to cover more advanced communication use cases.                                                                                                                                                              |
| **Power Management**                               | DIMO compatible devices must implement power management to prevent phantom drain of the vehicles it connects to, and efficiently manage being in “sleep” mode.                                                                                                                                                                                                                                 |
| **DBC Logger Configuration**                       | Each vehicle is different and provides different signals on the canbus. To handle this variety of messages, DIMO maintains an open repository \[[OPENDBC](https://github.com/DIMO-Network/opendbc)]. To be compatible with DIMO, the device must accept dynamic configuration of signals for filtering, parsing, and delivery to the protocol.                                                 |
| **Secure Runtime**                                 | Security is of highest importance to DIMO for both safety and security of the users. To provide an additional layer of safety to the car and the user, DIMO devices must run signed and verified code using secure boot mechanisms.                                                                                                                                                            |
|  **OTA Process**                                   | To be accepted into the program, the device manufacturer must routinely support and update their devices as new vulnerabilities are found. This must be able to be done via cellular connection.                                                                                                                                                                                               |

&#x20;

### Device Categories

The following device categories are supported by the DIMO Foundation, in line with the platform roadmap, and device support estimates which are published publicly.&#x20;

[Fleet Growth / Hardware deployment](https://docs.google.com/spreadsheets/d/1TQ6NSNOaHYb041JM6iUGnZGm9gjp5KONWvYI-LUaqM4/edit?usp=sharing)

The hardware team will be working directly with manufacturers to produce devices that fit the purchase price and performance specifications outlined for each.&#x20;

To incentivize the creation of devices in each category, the DIMO Foundation Hardware team will work with manufacturers to guarantee production and provide initial licenses according to the following target areas (subject to change based on interest / market feedback).&#x20;

![](https://lh5.googleusercontent.com/QmM-WZS1s68PdUe451\_EzRRpBkIjT7XHyX48KRYkxLlnX3ZhHqKo\_qfEcIFlX1bUBbMR0gNM3VXyWESHVQ5P27v36\_ArWANlocYzL0J7hhPt1QToUFg9T9phVfUocIHbN4X-dDoORNuP1QTe4A)

[DIMO V2: Fleet Black Box & OP Miner](https://docs.google.com/document/u/0/d/1Ve6fx32u4Ehg98KPeNM5bseoAwnn8hibrbrrE2oCaUc/edit)

#### Pairing Process&#x20;

Digital Infrastructure Inc will open-source the pairing code for the DIMOxAutoPi miner and mobile application, which can be used as a spec for any future pairing process using a standard bluetooth interface.&#x20;

#### Connectivity&#x20;

Digital Infrastructure Inc. has been approved to negotiate global rates, and has selected Twilio as the initial connectivity provider, an ISO27001 Certified and GDPR-compliant MVNO. Approved OEMs will be given access to acquire SIMs and bind connectivity agreements at the bulk purchase price, and can pass costs along to their customers through purchase and subscription agreements. &#x20;

Rates will be consistent throughout 2022, and connectivity will be re-auctioned in 2023.&#x20;

These rates can be applied to any approved device, and manufacturers can choose to go with their own connectivity provider if they choose, although additional integration work may be required to achieve Proof of Movement Certification.&#x20;

#### User Acceptance Testing&#x20;

Today, Digital Infrastructure Inc is responsible for testing and security - conducting thorough real-world and security penetration testing on the Alpha and Beta fleet units.&#x20;

DIMO Hardware will open applications to existing consumers, fleet users, and Pro Installers to test and certify new devices. Initial findings will be shared privately with hardware manufacturers, and subsequent rounds of testing (along with actual data) can be shared with the community prior to opening up presales. &#x20;

#### Community Engagement&#x20;

DIMO Retail will use official channels to notify the community of hardware approvals and certifications, and can assist with scheduling and promoting presales with our email list, Twitter, and Discord.&#x20;

&#x20;

For manufacturers without retail channels, distributor relationships can exist separate from DIMO certification, with the only requirement being that distributors must undergo a “Retail Certification” process prior to selling through DIMO-branded channels.

&#x20;

### Open Telematics Hardware Provider Licensing

DIMO-enabled hardware devices should be reliable, secure, and manufacturers should be aligned with the DIMO community.&#x20;

To achieve this we’re designing the hardware ecosystem to enable the following:&#x20;

·         Manufacturers who are long-term stakeholders in DIMO with skin in the game

·         A transparent governance process for approving and removing the licenses for hardware manufacturers&#x20;

·         Top quality devices integrated in a consistent way with the DIMO platform

·         Independent vetting of device performance related to cyber security and privacy&#x20;

#### Issuing Licenses & Paying Staking Fees

Hardware manufacturers must apply and share information about their qualifications with the DIMO \[d]Integrations composed initially by representatives of Digital Infrastructure inc., AutoPi, and other \[d]Integrations members.

Manufacturers must provide test units, data samples, and respond to questions from approved testers.&#x20;

Based on the readout from certified testers and hardware specialists, the community can vote for Manufacturer approval/rejection, and further information/clarifications can be requested before issuing a provisional DIMO hardware license.&#x20;

As the vote passes an official pre-sale can be conducted through the DIMO-approved channels (shop.dimo.zone).&#x20;

To join the blockchain, every device requires minting an NFT of the device itself, at that moment, there will be an automatic verification process to confirm the hardware manufacturer still has a valid license.

Licenses are non transferable NFTs that certify the manufacturer meets the qualifications required and checked by the DIMO Hardware Integrations Committee, and has been whitelisted for the production of compatible devices. Furthermore, the license certification requires the manufacturer to have previously staked a certain amount of $DIMO to hold them accountable for their performance.

To earn the “DIMO Certified” license and gain access to presale approval channels, device manufacturers must themselves stake 100,000 $DIMO, plus an additional amount of $DIMO per device to mint the NFT. E.g., if a hardware manufacturer sells 800 Dash cameras, they would have to acquire 74,000 $DIMO (e.g.:100,000 + (80 \* 800)).

For initial manufacturers building device categories underserved by the market, hardware manufacturers can earn temporary licenses through a loan from the DIMO foundation, provided that they produce devices that are approved by the committee.

The stake will be burned, distributed to the OEM and to \[d]Integrations in a variable, progressive way depending on the amount staked.

![](https://lh5.googleusercontent.com/p7KgYXGSXJDFFLd5M2PzdTCXUzMey6\_FPMWoJVu9k0w8JlVIVABpAsyvW7es05brBgCtO9MZEkGCYcWKUbi6m9f5mPacu26eaODmdNSsFnzCfj5McReG1ei7ZlvgXnyb0w7OVM04nCHLEOH2nw)

When the device is sold and installed, 25%-29.9% of the device-specific stake is burned (e.g.:20 $DIMO per device in this case) and the other 70.1%-75% will remain locked (e.g.:60 $DIMO per device in this case).

If the device malfunctions or is disconnected within two years after the initial connection, the amount of $DIMO locked would go entirely to the end user at a rate of 1/24th of the locked $DIMO per month. E.g., if the device malfunctions after 1 year, 30 $DIMO would go to the affected user.

If the device remains connected and in good working condition, both \[d]Integrations and the manufacturer would be rewarded.

From the 60 $DIMO locked, 3 $DIMO would go to \[d]Integrations at a rate of 1/24th each month for two years. The remaining 57 $DIMO would go to the hardware manufacturer at the same rate of 1/24th each month for two years.

[DIMO Miner Fulfillment](https://docs.google.com/spreadsheets/d/1K8v2HKdFob4Ul7mPbIikTBQn25Kg7tDCuLFpcQJG6Is/edit#gid=1585682634)

The initial 100,000 $DIMO for licensing will remain staked for as long as the manufacturer produces DIMO compatible devices.&#x20;

[Hardware manufacturer staking schedule](https://docs.google.com/spreadsheets/d/1Ie0q4-IfFv2QRLh-ApB80Zpbz2ChnqQAxzGOBBjHm\_8/edit#gid=0)

![](<../../.gitbook/assets/image (13).png>)

This aligns the manufacturer’s and incentives with those of the DIMO community as they will become $DIMO holders themselves and benefit when their product is reliable.&#x20;

Information on the performance of devices will become available to users through this process, which will allow them to make better decisions on future purchases based on manufacturer reputation.&#x20;

This also aligns the interests of the \[d]Integrations team to that of the end users, as they would be incentivized to make a thorough due diligence on the manufacturers to collect their $DIMO rewards.

#### Slashing & License Revocation

If an integration provider neglects their obligations as specified above, some or all of their stake may be forfeit (“slashed”) and their license may be suspended or revoked. Any $DIMO holder may issue a challenge per the DIMO arbitration procedure. If the \[d]Council, the name for DIMO’s arbitration council, sides in the favor of the challenger, all or some of the stake may be burned and/or given to affected users.

While \[d]Integrations, is both able to and expected to act as the challenger most often, they do not have the authority to unilaterally slash the manufacturers stake. That power lies with the \[d]Arbitration.&#x20;

Additionally, \[d]Integrations may unilaterally ban devices from the network (e.g., if they’re not secure and provide false data), suspend or revoke a manufacturer’s license at any time, or increase the manufacturer’s staking requirement above the minimum 100,000 $DIMO.&#x20;

Any manufacturer may renounce their license and receive back their staked $DIMO after six months if there are no successful challenges during that time frame.

#### How To Apply

Prospective integration providers must submit an application providing details about their business, their operating history, as well as specifications for the initial devices they intend to manufacture and/or software services they intend to provide. The initial application must contain specifications for at least one device design, test units, and data samples and/or a code repository and a functioning demo.

Licensed providers are able to submit additional and simplified applications for new devices and software methods at any time.

\[d]Integrations will design and launch the application and publish documentation outlining the process within 30 days following the passing of the DIP #3.

### Open Questions

#### Geographic Support&#x20;

DIMO will allow OEMs to register for support in the US, EU, and UK. Additional supported regions will be announced in the future.&#x20;

#### 3rd Party Certification ![AutoPi.io - CE Certified](file:///C:/Users/dm\_21/AppData/Local/Temp/msohtmlclip1/01/clip\_image008.png)

Devices should be automotive certified (CE/FCC)

**CE Certifications**

EN 301 489-1 v2.2.0

EN55025:2008

EN 50498 and Directive 2004/104/EC

ISO 7637-2:2011

EN 301 489-3 V2.1.1![AutoPi.io - FCC Certified](file:///C:/Users/dm\_21/AppData/Local/Temp/msohtmlclip1/01/clip\_image009.png)

**FCC Certifications**

Devices certified under the following standards:

FCC 47 CFR Part 15, Class A:10–1–17 Edition

&#x20;
