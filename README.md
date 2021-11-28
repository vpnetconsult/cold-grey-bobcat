# cold-grey-bobcat
Industrial IoT (IIoT) usecases

Step-By-Step Setup of a Helium Data-Only Hotspot that follows the guides available under

https://docs.helium.com/mine-hnt/data-only-guides/rak-concentrators/.

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


## Things that don't work, mPCIe

rather then having a single-piece concentrator component like the RAK2245 attached to your Raspberry (which you would need to re-assemble when changing frequency), the idea of a plug-n-play mPCIe Slot type solution seems intriguing. Here are a few things I figured are not working.

In the middle of the picture, due to the chip shortage, I got a hold of a RAK833-SX1301-SPI-AS923 mPCIe concentrator. Yeah!!
So I had two other components purchased before
- a no-name mPCIe-2-USB adaptor: so you can plugin the concentrator at the back of your Raspberry, even can built a stackable Rack
- a SEEED WM1302 Pi HAT: which let's you plugin the SEEED-WM1302-SPI-AS923 mPCIe concentrator

RAK833-SX1301-SPI-AS923 mPCIe + SEEED-WM1302-Pi HAT: Although mechanically these are standard interfaces, it doesn't work combining RAK with SEEED.
RAK833-SX1301-SPI-AS923 mPCIe with no-name mPCIe-2-USB adaptor: Should have read the small prints, in order to use mPCIe-2-USB you need the USB version of the RAK833 mPCIe. It's not a mechanical thing but some pins on the SPI only are missing.

![mPCIe](IMG_0979.jpg?raw=true "mPCIe stuff")


## Onboarding Step-By-Step

The 'endgame' is to have the data-only hotspot in your helium app same as with your other hotspots. See the detailed 11 Steps in the subfolder / Onboarding. I tried to make it as 'fool-proof' as possible. Let me know if you spot any issues.
