# cold-grey-bobcat
Industrial IoT (IIoT) usecases

Step-By-Step Setup of a Helium Data-Only Hotspot that follows the guides available under
https://docs.helium.com/mine-hnt/data-only-guides/rak-concentrators/
The hardware requirements are identical to a PoC Miner. You only run a different software that makes it a Data-Only hotspot with network packet forwarding.
There is a video link below I found of a guy that assembles a RAK2245 DIY miner. I haven't used this Kit but essentially it shows the assembly of all parts.

https://www.youtube.com/watch?v=DdnzSmJ5Fxg

We strictly stick to the list of Lora Concentrator listed there. I got a hold of RAK2245 but any other listed Concentrator should be fine too. The later software setup using the preconfigured Raspberry image let's you select the concentrator type. In principle it should be possible to reconfigure your data-only hotspot when you change to another concentrator as long as it is listed under the RAK

## Hardware Parts

Be mindful of the correct frequency for your region, you will likely encounter that most active Lora components for the common regions are SOLD OUT.

WisLink LPWAN Concentrator/RAK2245/Rpi HAT Edition/AS923
- HSCODE        : 8517629200
- Price         : $120
- Shipping      : $20
- Duty Tax (5%) : MYR 26.50
- SIRIM         : MYR 40.00  


## Onboarding Step-By-Step

The 'endgame' is to have the data-only hotspot in your helium app same as with your other hotspots. See the detailed 11 Steps in the subfolder / Onboarding. I tried to make it as 'fool-proof' as possible. Let me know if you spot any issues.
