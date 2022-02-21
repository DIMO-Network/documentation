---
description: How drivers and fleet operators can earn $DIMO
---

# Demand Signal

Driver rewards will be based on a combination of baseline and market demand for vehicle data and connectivity.&#x20;

**Baseline Demand Signal** refers to the concept of rewarding drivers based on how long they've been connected, what type of car they drive, and what types of data they provide, even if there is no end customer using their data. **This will be the sole driver issuance mechanic initially**. The goal here is to prime the network by incentivizing drivers to connect the types of cars and stream the types of data that we expect will be valuable to data consumers and app developers in the future.

**Market Demand Signal** refers to rewarding drivers based on what third parties are paying for their data. E.g., if Acme Corp subscribes to Alice's data for $10/month, Alice receives $10/month less a small protocol fee or burn (amount TBD).

In the early stages of DIMO's development, the vast majority of rewards will come from Baseline Demand Signal. As the network grows, this balance will likely shift the other way. This is comparable to other web3 networks like Helium, where their rewards from proof of coverage will shrink in comparison to rewards from data transfer over time.

### Rewards from Baseline Demand Signal

450,000,000 $DIMO (45% of the total supply) will be allocated to fund the Baseline Demand Signal reward pools. These pools will be issued over 40 years by issuing 1,300,000 $DIMO to users per week for the first year, with issuance decreasing by 15% each year. For more on the allocation and distribution curve over time, read [Token Distribution](token-distribution.md).

As implied above, the goal here is to allow actual market demand to gradually supplement and replace baseline demand, thus reducing and removing the need to inflate the circulating supply of $DIMO in perpetuity.

A weekly issuance was chosen because driving behavior varies dramatically by time of day (i.e., it’s concentrated during peak commuting hours). If the issuance protocol were to distribute $DIMO by the hour, then drivers would be under-compensated during rush hour (as the reward would be split between a high percentage of drivers) and overcompensated for driving at 3AM. A weekly issuance allows for a predictable issuance schedule, transaction fee optimization, and relatively frequent rewards distributions without incentivizing abnormal driving behavior.

To start, two different [dTeams](../governance/dteams.md) will oversee the distribution of baseline rewards. dCore will facilitate the distribution of half of the 1,300,000 $DIMO issued weekly. dGreen will facilitate the distribution of the other 650,000 $DIMO per a separate rewards formula aimed at incentivizing pro-social behavior.

![A visualization of the various baseline rewards pools](../.gitbook/assets/diagram.png)

Once the token distribution goes live on mainnnet, the weekly issuance will be allocated per the following methodology from each pool.

![](<../.gitbook/assets/Screen Shot 2022-02-21 at 12.48.24 PM.png>)

In year one, the dCore rewards pool will issue 650,000 $DIMO per week to users based on how many points they've earned as a percentage of all the points earned by all users. For example, if in a given week, you earn 1% of all of the points earned by all drivers, you receive 6,500 $DIMO (1% of the 650,000 weekly distribution). Drivers earn points based on how long they've maintained an active connection and the quality of their data connection.

Our aim is to:

* Reward and give control to those who show long-term support for DIMO;
* Incentivize a continuous data connection, which tells a richer story on driver behavior and vehicle performance when maintained over a long-period of time;
* Reward those with a hardware miner or Tesla's direct software connection because they provide better and more real-time vehicle data; and
* Avoid rewarding based on distance or time traveled as not to incentivize wasteful and unnecessary driving.

In this example, Alice earns 2,000 points for having been connected between 20 to 36 weeks and 7,500 points for having a [DIMO Data Miner](https://shop.dimo.zone) installed in her Mach-E which has already been [decoded](https://github.com/DIMO-Network/opendbc). Her total is 9,500 points for the week.

If there are 10,000 other cars connected to DIMO and each car averages 6,000 points that week, Alice has earned 0.0158% of all the points generated that week (9,500 ÷ 60,000,000). Therefore, she receives approximately 103 $DIMO from this pool (0.0158% \* the weekly 650,000 dCore $DIMO issuance).

![](<../.gitbook/assets/Screen Shot 2022-02-21 at 12.48.32 PM.png>)

Because Alice drives an electric vehicle, she is also eligible to earn $DIMO from the dGreen rewards pool, which also issues 650,000 $DIMO per week in year one. The Mach-E is a 100% electric vehicle so she earns 5,000 points. There are only 40 other 2021 Mustang Mach-E's connected to DIMO this week so she earns another 3,000 points for the rarity of her car. In addition to encouraging eco-conscious decisions, dGreen also wants to incentivize the connection of a diverse selection of electric vehicles.

In the example above, there are 6,000 electric and plug-in hybrid vehicles connected to DIMO. Alice's 8,000 points represent 0.0190% of all points (8,000 ÷ 42,000,000) meaning she receives approximately 124 $DIMO (0.0190% \* the weekly 650,000 dGreen $DIMO issuance).

![](<../.gitbook/assets/Screen Shot 2022-02-21 at 12.48.44 PM.png>)

Across both pools, Alice earned approximately 227 $DIMO in a week. If she continued to earn that amount each week, she would end the year with 11,790 tokens from her Mach-E.&#x20;

$DIMO token holders can vote to alter these rewards formulas, alter the issuance amounts, and create new pools. Below you can see earnings for a various hypothetical personas.

![](<../.gitbook/assets/Screen Shot 2022-02-21 at 12.53.06 PM.png>)

### Market Demand Signal

The exact launch timeline and methodology for distributing passthrough rewards from actual market demand will be determined by a future vote of $DIMO token holders.

Generally, we expect such a program to entail $DIMO flowing from data customers to data producers (drivers and fleet operators) based on the usage of their vehicle data and connectivity. This arrangement would be based on rates that the DAO negotiates with data consumers, who will most often be Data Unions (brokers). There will also be a small percentage of $DIMO that will be funnelled to the DIMO Foundation to fund future development or burned with each data sale transaction (exact terms TBD).

### Withdrawing rewards <a href="#eafc" id="eafc"></a>

Initially, DIMO will require a 7-day delay to withdraw tokens so various automated security checks can be performed. This will allow the DAO to challenge the authenticity of the data and validate that no duplicate or malicious actors are sending data into the network. This delay will not impact the availability of tokens for voting purposes. We hope to shorten and possibly eliminate this time lock with improved data verification protocols.



_The contract address for $DIMO is 0x5fab9761d60419c9eeebe3915a8fa1ed7e8d2e1b. Please always confirm that you are interacting with this contract address and not that of a fraudulent imitator. This webpage is making no guarantees about the nature of the DIMO DAO or the $DIMO token or its distribution, which are subject to change based on continued legal, tax, and other design considerations. $DIMO will launch as a governance token with no claim on financial rights and no economic value. Please triple check that any communications from DIMO are authentic as it’s common for scammers to try to trick you into sending them crypto or into revealing your private keys._
