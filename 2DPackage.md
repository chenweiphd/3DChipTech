# 2D Package

(Modified from Leo Zhi, UTMEL)

Currently, in the field of advanced packaging, there are three main types that can be distinguished: 2D packaging, 2.5D packaging, and 3D packaging. Each type has its own unique characteristics and applications, offering a wide range of possibilities for various industries. Through continuous research and development, these packaging techniques have evolved to meet the ever-growing demands of modern technology.

2D Packing is a computational problem that involves fitting a set of 2D objects into a container of fixed dimensions in the most efficient way possible. The goal is to minimize wastage of space and optimize the arrangement of objects.

Two important factors for categorizing electronic integration technologies are

 1. Physical structure

All chips and passive devices are physically installed on the substrate plane. The XY plane is in direct contact with chips and passive devices. Substrate wiring and holes are located below the XY plane

 2. Electrical connection (electrical interconnection)

All electrical connections must pass through the substrate (except for very few bonding points directly connected by bonding wire)

The chip integration primarily follows a 2D approach, where the transistors are integrated into the wafer plane. Similarly, PCB integration also follows a 2D approach, where electronic components are mounted flat on the PCB surface. Therefore, both chip and PCB integration can be considered as 2D integration. However, in-package integration presents a more complex scenario.

## 1 FOWLP
FOWLP (Fan-out Wafer Level Package) is a kind of WLP (Wafer Level Package), so we need to understand WLP wafer-level package first.

Before the emergence of WLP technology, the traditional packaging process was mainly carried out after the dicing of bare wafers, where the wafers were first diced and then packaged into various forms.

WLP was introduced around 2000, and there are two types: Fan-in and Fan-out.

After the packaging is completed, the wafer is cut and sliced. The size of the packaged chip is almost the same as the bare chip, so it is also called CSP (Chip Scale Package) or WLCSP (Wafer Level Chip Scale Packaging). These packages are in line with the market trend of light, small, short, and thin consumer electronics.

In the beginning, WLPs were mostly in Fan-in form, which can be called Fan-in WLP or FIWLP, and were mainly used for chips with small areas and low pin counts.

With the improvement of the IC process, the chip area shrinks, and the chip area cannot accommodate a sufficient number of pins. Therefore, the Fan-Out WLP package form, also known as FOWLP, was developed to make full use of RDL outside the chip area to make connections for more pins.

The flow of the FOWLP package is shown in the figure below.

![41297bc15341b72b3c6fc4a0f72e9336_ba35b3fa-2743-4518-80b2-b96df93d52ce](https://github.com/RIOSMPW/3DChipTech/assets/100336131/4b5613d6-f0bf-4db8-8cb3-97746b7fd85b)


FOWLP Packaging Process

### 1.1 InFO of TSMC

![image](https://github.com/RIOSMPW/3DPackageTech/assets/100336131/648af194-006c-4a10-ab3c-1fe99f816055)

InFO-of-TSMC

InFO (Integrated Fan-out) is a FOWLP IC packaging technology developed by TSMC in 2017. It is an integration on the FOWLP process, which can be understood as the integration of multiple chips Fan-Out process, while FOWLP favors the Fan-Out package process itself. InFO technology is similar to Fan-out technology used in most packaging plants and can be thought of as the integration of the multi-chip Fan-out process. The main distinction is that the silicon interposer has been removed, and some RDL layers have been used for concatenation (the A10 processor in the 2016 iPhone7, Taiwan Semiconductor 16nm FinFET process, and InFO technology).

InFO gives room for multiple chip integration and can be applied to RF and wireless chip packaging, processor and baseband chip packaging, and graphics processor and network chip packaging. The following diagram shows the comparison of FIWLP, FOWLP, and InFO.

![e7d76be07f9ff50fb222e96448914b4b_4a847eb5-6bcb-4d8b-8230-2ec0630d561d](https://github.com/RIOSMPW/3DChipTech/assets/100336131/ef6f33c1-0167-45c3-93d6-abd1f604c4e0)

FIWLP, FOWLP and InFO comparison schematic

### 1.2 eWLB of ASE

![image](https://github.com/RIOSMPW/3DPackageTech/assets/100336131/9804f64e-0d4b-475e-88f7-0086ff21f7f7)


Similar to TSMC InFO, both are Fan-out technologies

eWLB-of-ASE
In addition, there is a 2D+ integration

2D+ integration refers to the traditional stackable integration of chips connected by bonding lines. Some people may ask, chip stacking is not 3D, why should it be defined as 2D+ integration?

Mainly based on the following two reasons:

3D integration now primarily refers to integration via 3D TSV. To avoid misunderstanding, we refer to this traditional chip stacking as 2D+ integration.
Although the physical structure is 3D, the electrical interconnection must pass through the substrate, which means that the bonding wire must first be bonded to the substrate before the electrical interconnection can take place. This is equivalent to 2D integration. The improvement over 2D integration is stacking in structure, which can save packaging space, so it is called 2D+ integration.
Physical structure: All chips and passive devices are above the XY plane, some chips do not directly contact the substrate, and the wiring and holes on the substrate are below the XY plane.
Electrical Connection: All electrical connections must pass through the substrate (except for very few bonding points directly connected by bonding wire)

## 2 FOPLP
FOPLP (Fan-out Panel Level Package) is based on the idea and technology of FOWLP but uses a larger panel, so it can be mass-produced in a package several times larger than a 300 mm silicon wafer chip.

FOPLP technology is an extension of FOWLP technology, which is a Fan-Out process on a larger square carrier board, hence the name FOPLP packaging technology.

Currently, FOPLP uses a 24×18-inch (610×457mm) PCB carrier board, which is about four times the area of a 300 mm silicon wafer. Therefore, it can be simply considered that in a single process, it is possible to mass-produce 4 times more IC packages than 300 mm silicon wafers.

Like the FOWLP process, the FOPLP technology can integrate the front and backstages of the packaging process and can be considered as a single package process, thus significantly reducing production and material costs. The figure below shows the comparison between FOWLP and FOPLP.

![8789067a2baf256ecca9e3cfbbf07bdf_d6a043a3-7cad-4c2a-b5d3-0bfda114f2c5](https://github.com/RIOSMPW/3DChipTech/assets/100336131/c9c1e323-559f-43c4-8aa0-8c73d8c3c119)

Comparison of FOWLP and FOPLP

FOPLP adopts the production technology on PCB for RDL production, its line width and line pitch are currently greater than 10um, and SMT equipment is used for chip and passive device placement. Since its panel area is much larger than the wafer area, it can package more products at one time. Compared with FOWLP, FOPLP has greater cost advantages. At present, the world's major packaging companies, including Samsung Electronics and Sun and Moon, are actively involved in FOPLP process technology.

