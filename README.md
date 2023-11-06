# manta-ray-active-vacuum-tag

## About ##
This repository details ongoing research and development work by [Arribada](https://arribada.org) to develop an active vaccum (suction) cup tag, primarily to provide a non-invasive means of attaching scientific instruments to oceanic manta rays i.e accelerometers, video cameras or other instruments to advance scientific research.

![manta_vaccum_tag_github](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/05be5ccb-5a90-4966-b3cb-92b85e30428a)

## Description ##
The design specification of the payload was to primarily generate a vaccum underwater, removing water and air trapped within a vaccum cup when applied to the surface of a target animal quickly and efficiently. To achieve this, the payload itself needed to be slightly positively buoyant to aid recovery after being a) mechanically vented through the use of a corrodable plug to fill the vaccum with water and thus detach, or b) retained in place via a watertight / airtight seal until otherwise vented via a mechanical process.

Early iterations of the design utilised a modified commerical vaccum cup insert, with an attempt to reduce total weight made by milling away surface metal of the internal disk. Ultimately the overall weight and need to include additional syntactic foam to increase buoyancy required a custom ABS insert to be CNC milled instead, replacing the metal off-the-shelf variant. An example of a typical commercial vaccum cup insert with vaccum socket has been provided below. Typically, the weight of a vaccum cup insert is not a defining factor if used in a vaccum assembly line, however in our case the weight needed to be reduced significantly.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/f21fa3f8-925b-4340-a19b-fe4403c5a28f)

## Preparing the custom vaccum cup insert ##

To reduce the overall weight of the tag and to increase buoyancy we developed a custom ABS vaccum cup insert, filled with pre-cut syntactic foam, thus essentially creating a positively buoyant vaccum insert that would replace the commerical off the shelf variant (described above) that was too heavy to utilise. All CNC STEP files can be found in the hardware folder of this repo.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/64efab61-bb60-437e-abba-72799c4fda11)

When milling with a suitable CNC machine, the external (top) face of the insert needs to be milled flush (+/- 0.1mm tolerance) with a step on the lip to fit the FiPA vaccum cup (see below). In the graphic below the venting hole can be seen next to the central air extraction hole. A 1/4 BSPP non-return valve (RS PRO Non Return Valve, 10mm Tube Outlet - 144-2704) is attached after tapping the hole with a 1/4 tapping tool. Use plumbing tape (PTFE Tape) on the threads to ensure a watertight seal and secure with a 1/4 BSPP locking nut on the internal side (RS PRO Stainless Steel Locknut, 1/4 BSPP - 762-1184).

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/724b518a-190d-4bf2-88e8-f1b08b3be5be)

Alignment rings should be greased in a synthetic lubricant to help guide the nitrile rubber vaccum cup into position. Note - use a good amount of synthetic lubricant, such as super lube multi-purpose synthetic grease on the centre hole to help push the nitrile rubber inner ring into place. Without grease it can be quite challenging, but with grease it's possible to ease it in slowly, working your way around in a circle until the entire inner ring is flush with the ABS disk.

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/ede2a2b6-d2db-44d8-a66f-d85246c28b99)

The FiPA nitrile rubber vaccum cup we selected is designed for stacking partially air-permeable plate materials, so we selected it to help work with the manta's slime layer that we would ultimately need to attach to. We also selected this type of cup as it has a soft sealing lip made of abrasion-resistant nitrile and has a large surface area, although we intend to replace this part for a ClingTech variant in the near future (testing is still underway) that may enhance attachment further. 

![image](https://github.com/arribada/manta-ray-active-vacuum-tag/assets/6997400/70bb4b57-a766-4120-9486-88b3ad045970)

## Preparing the multi-jet fusion 3D printed body ##










