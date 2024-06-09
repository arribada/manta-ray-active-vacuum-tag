# Manta ray active vacuum tag #
## Version 1.02 | June 2024
![manta_tag](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/136ec232-e82c-4b59-bbe8-06c49197a670)

## About ##
This repository details ongoing research and development work by [Arribada](https://arribada.org) to develop an active vaccum (suction) cup tag, primarily to provide a non-invasive means of attaching scientific instruments to oceanic manta rays i.e accelerometers, video cameras or other instruments to advance scientific research conducted by the [Bureau of Ocean Energy Management](https://www.boem.gov/).

## Licencing ##
All hardware designs, files, assets and schematics in this repository are licenced under CERN OHL v1.2. Documentation is licenced under GPLv3.

## Active vaccum cup "tadpole" design ##
![manta_vaccum_tag_github](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/05be5ccb-5a90-4966-b3cb-92b85e30428a)

## Purpose ##
This tag was developed to provide a non-invasive means of attaching biologging instruments to oceanic manta rays through by attaching a vaccum cup on the manta's skin. It is primarily intended for attachment in-water by scuba divers, although a pole-based attachment mechanism is under development. The pole-based method will provide a means to attaching the tag from a vessel when mantas are at the surface.

The tag has been designed to fit Arribada's open source [Horizon ARTIC R2 Argos satellite / GNSS transmitter](https://arribada.org/horizon-gps-tracking/) to provide satellite positioning for recovery when on the surface. Other payloads, such as accelerometers, of optional VHF pingers can be fitted to either side of the tag's cylindrical mounting holes. 

The design files in this repository contain all of the components and necessary to build the physical tag. You are free to select your own electronics / payloads, or to use the Horizon transmitter which fits the tag natively.

## Description ##
The design specification of the payload was to primarily generate a vaccum underwater, removing water and air trapped within a vaccum cup when applied to the surface of a target animal quickly and efficiently. To achieve this, the payload itself needed to be slightly positively buoyant to aid recovery after being a) mechanically vented through the use of a corrodable plug to fill the vaccum with water and thus detach, or b) retained in place via a watertight / airtight seal until otherwise vented via a mechanical process.

Once on the surface, the tail of the tag should point towards the sky as it is the lightest part of the instrument. The base remains in the water carrying the payloads, exposing the whip antenna in the tail and allowing recovery by VHF (pinger) or Argos telemetry using an embedded [Arribada Horizon satellite transmitter](https://arribada.org/product/arribada-horizon-artic-r2-developers-kit/).

Early iterations of the design utilised a modified commerical vaccum cup insert, with an attempt to reduce total weight made by milling away surface metal of the internal disk. Ultimately the overall weight and need to include additional syntactic foam to increase buoyancy required a custom ABS insert to be CNC milled instead, replacing the metal off-the-shelf variant. An example of a typical commercial vaccum cup insert with vaccum socket has been provided below. Typically, the weight of a vaccum cup insert is not a defining factor if used in a vaccum assembly line, however in our case the weight needed to be reduced significantly.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/f21fa3f8-925b-4340-a19b-fe4403c5a28f)

# Manufacturing the Manta ray active vacuum tag #
## Version 1.02 ##

We recommend that you inspect the [bill of materials (BOM)](https://github.com/arribada/manta-ray-active-vacuum-tag/blob/main/Hardware/BOM/Manta%20active%20vaccum%20tag%20BOM.xlsx) necessary to build the tag, inspect the 3D printable assets, the CNC millable assets, and all of the necessary components required to develop and test the tag before proceeding. 

The tag consists of a 3D printable payload holder, typically printed in nylon (PA 11), attached to an ABS vaccum insert that are both printable and millable on suitable desktop 3D printers and mills (i.e. the Bambu X1 that supports nylon and the Carvera Desktop CNC). If you don't have access to suitable 3D printers or CNC machines the files can readily be printed and milled by third parties.

All other required components, such as the vacuum cup, air hose, venturi vacuum generator and Prevost quick attachment adapter are noted in the BOM and can be purchased from multiple online retailers.

## Step 1. Preparing the custom vaccum cup insert ##

The tag was designed to attach to and support the use of a Fipa ref.102.160.380.4 vacuum cup, a 160mm diameter cup originally designed to lift rough materials (sawn wood or materials with rough or uneven surfaces). Fipa cups can be purchased from any Fipa authorised supplier. We purchased our cups from Hennig UK Ltd, who selected the cup based on our requirements - size, grip and suitability for us to redesign a lighter open source vacuum insert to replace the metal insert that is typically used with standard vacuum machinery.

To reduce the overall weight of the tag and to increase buoyancy it was necessary to develop a custom ABS vaccum cup insert, filled with pre-cut syntactic foam, thus essentially creating a positively buoyant vaccum insert to replace the metal commerical off-the-shelf variant (described above) that was too heavy to utilise. Our re-designed insert fits the Fipa ref.102.160.380.4 vacuum cup and can be CNC milled in ABS using the supplied STEP files in the [/hardware](https://github.com/arribada/manta-ray-active-vacuum-tag/tree/main/Hardware) folder of this repository.

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

## Step 3. Assembling and preparing the air system and vacuum components ##

The following diagram illustrates each stage of the air system, identifying the positioning of vacuum components.

![manta_ray_air_system_assembly_stages](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/e871ccb6-f7e6-451c-be50-13c66b2ba15d)

### Stage 1 - Air tank ###

A standard 232 Bar scuba diving pony air cylinder can be used to provide air pressure to the system. A pony bottle is well suited as it can be carried by a diver as a seperate cylinder when diving to attach the tag to the manta ray. 

### Stage 2 - Air hose from cylinder to air gun ###

Install a suitable air hose and tubing. Tubing length can be 1m in length as it will only need to provide adequate distance from the cylinder to the air gun held on an outstretched air of the diver. The diver will operate the air gun to provide compressed air, which will be reversed by the venturi generator creating suction to remove water from beneath the vaccum cup.

### Stage 3 - Secure the air hose line ###

Install or locate a suitable position for the air gun to be attached to the diver's BCD as the diver may be in the water for some time waiting to identify a suitable manta ray to tag. A quick release mechanism is recommended, enabling the diver to move freely in the water without the hose dragging.

### Stage 4 - Tighten and maintain valves ###

Before tagging, test that your valves are clean and adequately tight as a loss of pressure can affect the speed in which the tag can attached if the venturi is supplied with less pressure that is it expecting.

### Stage 5 - Air gun ###

A standard air gun nozzle / convertor for scuba tanks works well to provide the compressed air source. [This is the air gun](https://www.diversdirect.com/p/quick-release-metal-air-blower-gun) utilised during our tests.

### Stage 6 - Air hose valve and venturi valve ###

Select a suitable valve to connect to your air gun's outlet that allows you to fit 8mm OD (outer diameter) and 6mm (inner diameter) tubing, as the tubing will need to fit a G1/8 threaded valve on the venturi

### Stage 7 - Air hose to venturi ###

The air hose should have a G1/8 valve fitted to mate with the air supply in (E) threaded valve socket on the venturi.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/17770c8a-8579-49ae-bd6f-a22fedddd7a4)

### Stage 8 - Valve maintenance, air in ###

Salt will collect in the valves of the venturi vacuum and will ultimately reduce pressure. Ensure tubes and the venturi's valves are cleaned after deployment in saltwater.

### Stage 9 - Venturi (Vacuum generator)

Connect the air hose from the air gun to valve E (G1/8) and connect another hose from the vacuum port J (G1/4) using the 10mm ID, 12mm OD tubing. The venturi will create a vacuum and remove air / liquid through the exhaust when over 3.5 bar of pressure from a compressed air source is applied. You can test that your venturi is working by applying compressed air and observing the tag sink down on a flat surface (i.e. a table) as air is removed from under the vacuum cup. In water you will see air bubbles escaping from the exhaust. The black exhaust port is a silencer used with air and can be removed if used in water as it does not function in the same way when used with liquids.

### Stage 10 - Valve maintenance, water out ###

Salt will collect in the valves of the venturi vacuum and will ultimately reduce pressure. Ensure tubes and the venturi's valves are cleaned after deployment in saltwater.

### Stage 11 - Step down adapter ###

The prevost quick release S1 adapter requires 8mm tubing, so a reducer nipple is required to step down the 12mm tubing (OD) from the venturi G1/4 valve socket. Connect the reducer nipple inline using the Festo adapter.

### Stage 12 - Connect tubing to the Prevost S1 quick release coupler ###

Connect the tubing to the adapter on the Prevost S1 and then connect the S1 to the tag's quick release adapter. You have now completed assembling the air system. By pressing the quick release button on the Prevost S1 the adapter will release the coupler and detach the tag. Pushing the Prevost back onto the tag's connector will re-attach the air system to the tag.

## Step 4. Preparing and installing the buoyancy aid (closed cell foam).

As noted in Step 1, the use of syntactic foam is necessary to generate the buoyancy required for the tag to float when dislodged from the manta for recovery. The tail of the tag lifts the tip up when on the water's surface, pointing any antennas you attach (i.e. Argos satellite antenna) towards the sky. The heavier vacuum disk and Prevost S1 coupler point down. Syntactic form should be added to the cavity of the tag's body and a thin layer applied inside the vacuum disk insert (see Step 1) to reduce overall weight. The cutting guide below identifies the dimensions of the foam required to cut and fill the cavity. It is recommended to print a template file using a 3D printer and cut / sandpaper Subsea Buoyancy Foam (R-3318) to fill the cavity.

![Foam_cutting_template_bottom](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/bb202f7a-a018-4efd-ad75-a430cf5353e0)

![Foam_cutting_template_top](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/164018b3-ab45-4b5c-aed3-4302a24e5d1d)


# Optional pole release mechanism #
## Step 5. (Experimental) Preparing the multi-jet fusion 3D printed pole mount head ##

An optional 3D printed pole mount that fits the provost is available to trial. Print the pole head mount (see BOM) using MJF as the process and PA 11 as the material. PA 12 should also be suitable. Once printed, use a tapping kit to manually tag the top hole using an M9 x 1.25 tapping bit. Next, insert a 1/4" female screw adapter into the socket using pliers. 

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/735b4dfc-aba2-4b41-ae69-344309b92570)

A stainless steel 360 degree swivel camera mount adapter can then be attached to the pole mount head and to a suitable telescopic boom pole that has a 1/4" thread embedded, such as the range of fiberglass poles from compositepoles.co.uk.

To fit and seat the bicycle brakes, first slot the Prevost S1 coupler into the pole head slot. Use the grip indents to guide it into place. Then slow the two M8 x 60mm socket flanged button screws through the bottom holes and secure the brakes in place using 4 x M8 hexagon nuts to align the brake in place.

## Continued research ##

We are continuing to explore the material properties of the nitrile rubber in comparison to other vaccum cup materials, notably ClingTech vaccum cups that we believe may enhance the longevity of attachments. To date this tag design has achieved a 4 hour attachment, with a goal to exceed 24 hours as the design is further enhanced. An internal Arribada Horizon Argos ARTIC R2 transmitter can also be loaded into the tag to enable recovery of the tag in the open ocean using Argos satellite telemetry (doppler).

Once completed and tested, the final pole attachment design will be uploaded to this repo to aid attachment. 

### Pole attachment design ###

![manta_ray_pole_102_jpeg](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/5c9360f1-87f2-42c4-b52e-396013209922)

 











