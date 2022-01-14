---
description: Details on the DIMO x AutoPi Hardware Miner
---

# Hardware Device

### Where can I find my car’s OBD2 port?&#x20;

The OBD2 port is usually under the front console on the driver’s side of the vehicle, but there can be a lot of variation from car to car. Check out [this link](hardware-device.md#where-can-i-find-my-cars-obd2-port) to identify where your OBD2 port is.&#x20;

### Will the device cause any issues for my car? Is it safe?

DIMO does compatibility testing with all vehicles we support. DIMO-approved 3rd party hardware devices are currently passive listeners only. This means that they cannot be used to control your vehicle.&#x20;

### How do you validate the data?&#x20;

As a user, you will sign the data with your wallet and DIMO will validate the signature when data is received. Data is watermarked for third-party consumers.&#x20;

### How are you going to get CAN codes?&#x20;

DIMO is an open source supporter and contributor, building on projects like [openDBC](https://github.com/commaai/opendbc), CANserver, and CANBusHack to compile and maintain a library of CAN codes. Want to contribute? [Click here](https://discord.gg/DKPsxDuPkp).

### Will it drain my car battery?&#x20;

The device goes into a low power sleep mode shortly after you stop driving, so you will not see any vampire battery drain from the device.&#x20;

### Is it always connected?&#x20;

The device is always connected. As mentioned above it only uses a tiny amount of power and won’t drain your battery at all.&#x20;

### Can I use it to turn my car on?

Turning your car on is not currently supported. It is possible to add this functionality for certain vehicles in the future.&#x20;

### Who is paying for the cellular costs?&#x20;

DIMO is paying for cellular costs of transmitting data from your vehicle for at least 12 months. The DIMO DAO will decide how ongoing costs will be handled after the initial 12 month period.

### What happens if I’m driving in an area without cellular reception?&#x20;

The data will be saved on the device until you return to an area with cellular connectivity.&#x20;

### Can I use this with my another plug-in device?&#x20;

Vehicles only come with one OBD2 port, but we have validated in the alpha fleet that OBD-II splitters like [this model](https://www.amazon.com/dp/B0711LGRGQ/ref=redir\_mobile\_desktop?\_encoding=UTF8\&aaxitk=9f03e8ddf53c4cf1de9f5153355cc895\&hsa\_cr\_id=5478793350401\&pd\_rd\_plhdr=t\&pd\_rd\_r=74e2c482-041e-4bb9-9973-d3e69abad07e\&pd\_rd\_w=cksmI\&pd\_rd\_wg=uwz5O\&ref\_=sbx\_be\_s\_sparkle\_mcd\_asin\_0\_title) will work on all cars tested so far.

In the future, DIMO will work to build partnerships with insurance companies so that you can provide them the data they would need to offer discounts (but no other data!).
