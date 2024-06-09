# Manta ray active vacuum tag
## Version 1.02 | June 2024
![manta_tag](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/136ec232-e82c-4b59-bbe8-06c49197a670)

## About ##
This repository details ongoing research and development work by [Arribada](https://arribada.org) to develop an active vaccum (suction) cup tag, primarily to provide a non-invasive means of attaching scientific instruments to oceanic manta rays i.e accelerometers, video cameras or other instruments to advance scientific research conducted by the [Bureau of Ocean Energy Management](https://www.boem.gov/).

## Licencing ##
All hardware designs, files, assets and schematics in this repository are licenced under CERN OHL v1.2. Documentation is licenced under GPLv3.

## Active vaccum cup "tadpole" design ##
![manta_vaccum_tag_github](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/05be5ccb-5a90-4966-b3cb-92b85e30428a)

## Description ##
The design specification of the payload was to primarily generate a vaccum underwater, removing water and air trapped within a vaccum cup when applied to the surface of a target animal quickly and efficiently. To achieve this, the payload itself needed to be slightly positively buoyant to aid recovery after being a) mechanically vented through the use of a corrodable plug to fill the vaccum with water and thus detach, or b) retained in place via a watertight / airtight seal until otherwise vented via a mechanical process.

Once on the surface, the tail of the tag should point towards the sky as it is the lightest part of the instrument. The base remains in the water carrying the payloads, exposing the whip antenna in the tail and allowing recovery by VHF (pinger) or Argos telemetry using an embedded [Arribada Horizon satellite transmitter](https://arribada.org/product/arribada-horizon-artic-r2-developers-kit/).

Early iterations of the design utilised a modified commerical vaccum cup insert, with an attempt to reduce total weight made by milling away surface metal of the internal disk. Ultimately the overall weight and need to include additional syntactic foam to increase buoyancy required a custom ABS insert to be CNC milled instead, replacing the metal off-the-shelf variant. An example of a typical commercial vaccum cup insert with vaccum socket has been provided below. Typically, the weight of a vaccum cup insert is not a defining factor if used in a vaccum assembly line, however in our case the weight needed to be reduced significantly.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/f21fa3f8-925b-4340-a19b-fe4403c5a28f)

# Manufacturing the Manta ray active vacuum tag #
# Version 1.02"

We recommend that you inspect the bill of materials (BOM) necessary to build the tag, inspect the 3D printable assets, the CNC millable assets, and all of the necessary components required to develop and test the tag before proceeding. 

The tag consists of a 3D printable payload holder, typically printed in nylon (PA 11), attached to an ABS vaccum insert that are both printable and millable on suitable desktop 3D printers and mills (i.e. the Bambu X1 that supports nylon and the Carvera Desktop CNC). If you don't have access to suitable 3D printers or CNC machines the files can readily be printed and milled by third parties.

All other required components, such as the vacuum cup, air hose, venturi vacuum generator and Prevost quick attachment adapter are noted in the BOM and can be purchased from multiple online retailers.

The tag can be manufactured in 

## Step 1. Preparing the custom vaccum cup insert ##

To reduce the overall weight of the tag and to increase buoyancy we developed a custom ABS vaccum cup insert, filled with pre-cut syntactic foam, thus essentially creating a positively buoyant vaccum insert that would replace the commerical off the shelf variant (described above) that was too heavy to utilise. All CNC STEP files can be found in the hardware folder of this repo.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/64efab61-bb60-437e-abba-72799c4fda11)

When milling with a suitable CNC machine, the external (top) face of the insert needs to be milled flush (+/- 0.1mm tolerance) with a step on the lip to fit the FiPA vaccum cup (see below). In the graphic below the venting hole can be seen next to the central air extraction hole. A 1/4 BSPP non-return valve (RS PRO Non Return Valve, 10mm Tube Outlet - 144-2704) is attached after tapping the hole with a 1/4 tapping tool. Use plumbing tape (PTFE Tape) on the threads to ensure a watertight seal and secure with a 1/4 BSPP locking nut on the internal side (RS PRO Stainless Steel Locknut, 1/4 BSPP - 762-1184).

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/724b518a-190d-4bf2-88e8-f1b08b3be5be)

Alignment rings should be greased in a synthetic lubricant to help guide the nitrile rubber vaccum cup into position. Note - use a good amount of synthetic lubricant, such as super lube multi-purpose synthetic grease on the centre hole to help push the nitrile rubber inner ring into place. Without grease it can be quite challenging, but with grease it's possible to ease it in slowly, working your way around in a circle until the entire inner ring is flush with the ABS disk.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/ede2a2b6-d2db-44d8-a66f-d85246c28b99)

The FiPA nitrile rubber vaccum cup we selected is designed for stacking partially air-permeable plate materials, so we selected it to help work with the manta's slime layer that we would ultimately need to attach to. We also selected this type of cup as it has a soft sealing lip made of abrasion-resistant nitrile and has a large surface area, although we intend to replace this part for a ClingTech variant in the near future (testing is still underway) that may enhance attachment further. 

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/70bb4b57-a766-4120-9486-88b3ad045970)

## Step 2. Preparing the multi-jet fusion 3D printed body ##

The body of the tag is constructed in two halves (all STEP files are available in the hardware folder of this repo). The material used is PA 12, using either selective laser sintering (SLS) or multi-jet fusion 3D printing processes to form the body. PA 12 is porous, but as we are attaching payloads seperately we don't need to worry about water ingress - instead the body forms a hydrodynamic structure in which to hold the payloads, syntactic foam and push water over the air hose coupler in the centre to minimise drag. 

The image below details the assembly of the body. Accu stainless steel M4 socket flanger screws (50mm and 30mm) are used to attach the 3D printed body to the CNC milled ABS vaccum cup insert / base. Foam is cut and place in the internal cavity. Based on your choice of payload (weight), the foam can be removed or topped up as necessary to balance the tag and provide a slight amount of positive buoyancy. Mounting holes on the ABS insert are drilled to M3 in size ready to be tapped to M4 using a tapping tool. Once tapped you should drill the mounting holes out slightly in the 3D printed SLS leaving a little bite so there is additional grip still and the hole is tight to accept the screw and secure the body in place.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/570afa8d-255b-48c4-9ef0-5f171b59c605)

A complete bill of materials is available [here](https://github.com/arribada/manta-ray-active-vacuum-tag/tree/main/Hardware) to reconstruct the tag. It should be possible to replicate the tag with access to a 3D printer, 3-axis CNC machine and a basic workbench to aid tapping the threads and installing the air hose coupler.

It's important to use a stainless steel Prevost coupler vs the standard variant as the ball-bearings inside the coupler are brass vs stainless steel and will rust over time when exposed to salt water. The image below shows a Prevost coupler attached to the tag. The green button can be pressed with a single hand when in the water to detach the coupler after air has been removed using a venturi inline in the airhose. We used an Air Engineering Controls Ltd Vacuum Pump, 19.1mm nozzle , 847mbar 3398L/min venturi connected to a standard compressed air scuba tank. 

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/dafd4b76-2c17-4042-8482-f6b6579ad596)

A pole attachment method using a modified bike break to depress the green button remotely is currently being design. This will enable the tag to be attached to manta rays from a boat within a few meters. Preparation of the current design has been described below.

## Step 3. Preparing the multi-jet fusion 3D printed pole mount head ##

Print the pole head mount (see BOM) using MJF as the process and PA 11 as the material. PA 12 should also be suitable. Once printed, use a tapping kit to manually tag the top hole using an M9 x 1.25 tapping bit. Next, insert a 1/4" female screw adapter into the socket using pliers. 

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/735b4dfc-aba2-4b41-ae69-344309b92570)

A stainless steel 360 degree swivel camera mount adapter can then be attached to the pole mount head and to a suitable telescopic boom pole that has a 1/4" thread embedded, such as the range of fiberglass poles from compositepoles.co.uk.

To fit and seat the bicycle brakes, first slot the Prevost S1 coupler into the pole head slot. Use the grip indents to guide it into place. Then slow the two M8 x 60mm socket flanged button screws through the bottom holes and secure the brakes in place using 4 x M8 hexagon nuts to align the brake in place.

## Step 4. Assembling the body of the tag and installing vacuum components ##

-

## Continued research ##

We are continuing to explore the material properties of the nitrile rubber in comparison to other vaccum cup materials, notably ClingTech vaccum cups that we believe may enhance the longevity of attachments. To date this tag design has achieved a 4 hour attachment, with a goal to exceed 24 hours as the design is further enhanced. An internal Arribada Horizon Argos ARTIC R2 transmitter can also be loaded into the tag to enable recovery of the tag in the open ocean using Argos satellite telemetry (doppler).

Once completed and tested, the final pole attachment design will be uploaded to this repo to aid attachment. 

### Pole attachment design ###

![manta_ray_pole_102_jpeg](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/5c9360f1-87f2-42c4-b52e-396013209922)

 











