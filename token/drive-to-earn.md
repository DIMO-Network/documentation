---
description: How drivers and fleet operators can earn $DIMO
---

# Demand Signal

Driver rewards will be based on a combination of baseline and market demand for vehicle data and connectivity.&#x20;

**Baseline Demand Signal** refers to the concept of rewarding drivers based on how many miles they drive, what type of car they drive, and what types of data they provide, even if there is no end customer using their data. **This will be the sole driver issuance mechanic initially**. The goal here is to prime the network by incentivizing drivers to connect the types of cars and stream the types of data that we expect will be valuable to data consumers and app developers in the future.

**Market Demand Signal** refers to rewarding drivers based on what third parties are paying for their data. E.g., if Acme Corp subscribes to Alice's data for $10/month, Alice receives $10/month less  protocol fees.

In the early stages of DIMO's development, the vast majority of rewards will come from Baseline Demand Signal. As the network grows, this balance will likely shift the other way. This is comparable to other web3 networks like Helium, where their rewards from proof of coverage will shrink in comparison to rewards from data transfer over time.

### Rewards from Baseline Demand Signal

As outlined in [Token Distribution](token-distribution.md), 450,000,000 $DIMO (45% of the total supply) will be allocated to fund the Baseline Demand Signal reward pool. This pool will be issued over 40 years by issuing 1,300,000 $DIMO per week for the first year, with issuance decreasing by 15% each year anniversary.

As implied above, the goal here is to allow actual market demand to gradually supplement and replace baseline demand, thus reducing and removing the need to inflate the circulating supply of $DIMO in perpetuity.

Once the token distribution goes live on mainnnet, the weekly issuance will be allocated per the following methodology:

Throughout each week drivers will earn points depending on the miles and minutes they drive, the types of data they opt-in to provide, and the rarity of their make and model. They will then earn $DIMO tokens based on the percentage of total points that they received for that period. For example, if Alice earns 500,000 points in a week, and a total of 5,000,000,000 points are earned across all drivers in that same week, Alice earns 130 $DIMO (0.01% of points \* 1,300,000 $DIMO issued).

![Planned points formula for allocating $DIMO weekly rewards from the simulated market demand pool](<../.gitbook/assets/Screen Shot 2022-01-20 at 3.56.08 PM.png>)

Curious how this might function in practice? Take a look at the following hypothetical payouts for a week where 1,500,000,000 points were generated across all drivers. Remember, this is only showing rewards from Baseline Demand Signal and is not taking into account any rewards earned from Market Demand Signal (as described further down).

Curious how this might function in practice? Take a look at the following hypothetical payouts for a week where 1,500,000,000 points were generated across all drivers. Remember, this is only showing rewards from Simulated Demand Signal and is not taking into account any rewards earned from Market Demand Signal (as described further down).

![Hypothetical distributions by persona assuming all users collectively earned 1.5b points in that week](<../.gitbook/assets/Screen Shot 2022-01-04 at 4.14.41 PM.png>)

It's important to note that vehicle data is NOT being sold or provided to 3rd party applications prior to the establishment of a Data Union, which will allow users to opt-in to sharing data and receiving Market Demand Signal rewards. Still, we've created our rewards formula to incentivize drivers to stream data that we expect will be valuable in the future. To explain the logic of the points multipliers and cap:

* Having a rare vehicle (make/model/year) helps us onboard a diverse set of vehicles;
* Having the hardware miner connected is valuable because it makes vehicle data richer and more secure;
* Electric vehicle batteries are new technology and their data is valuable; and
* Limiting unnecessary driving: we don't want to incentivize people to drive around the clock purely for the sake of earning $DIMO and we want to make sure professional drivers don't dominate the distribution.

A weekly issuance was chosen because driving behavior varies dramatically by time of day (i.e., it’s concentrated during peak commuting hours). If the issuance protocol were to distribute $DIMO by the hour, then drivers would be under-compensated during rush hour (as the reward would be split between a high percentage of drivers) and overcompensated for driving at 3AM. A weekly issuance allows for a predictable issuance schedule, gas optimization, and relatively frequent rewards distributions without incentivizing abnormal driving behavior.

![](<../.gitbook/assets/Untitled 2.png>)

### Market Demand Signal

The exact launch timeline and methodology for distributing passthrough rewards from actual market demand will be determined by a future vote of $DIMO token holders.

Generally, we expect such a program to entail $DIMO flowing from data customers to data producers (drivers and fleet operators) based on the usage of their vehicle data and connectivity. This arrangement would be based on rates that the DAO negotiates with data consumers, who will most often be Data Unions (brokers). There will also be a small percentage of $DIMO that will be burned with each data sale transaction.

### Withdrawing rewards <a href="#eafc" id="eafc"></a>

Initially, DIMO will require a 7-day delay to withdraw tokens so various automated security checks can be performed. This will allow the DAO to challenge the authenticity of the data and validate that no duplicate or malicious actors are sending data into the network. This delay will not impact the availability of tokens for voting purposes. We hope to shorten and possibly eliminate this time lock with improved data verification protocols.



_The contract address for $DIMO is 0x5fab9761d60419c9eeebe3915a8fa1ed7e8d2e1b. Please always confirm that you are interacting with this contract address and not that of a fraudulent imitator. This webpage is making no guarantees about the nature of the DIMO DAO or the $DIMO token or its distribution, which are subject to change based on continued legal, tax, and other design considerations. $DIMO will launch as a governance token with no claim on financial rights and no economic value. Please triple check that any communications from DIMO are authentic as it’s common for scammers to try to trick you into sending them crypto or into revealing your private keys._
