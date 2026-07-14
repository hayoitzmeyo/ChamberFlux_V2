# ChamberFlux V2 Fan Module

**A compact, adjustable chamber-circulation module for enclosed FDM printers**

ChamberFlux V2 is designed to improve bulk air transport inside printer enclosures, extending the effective reach of existing filtration systems with universal integration.

<p align="center">
  <img src="media/render-front.png" alt="Front render of ChamberFlux V2" width="47%">
  <img src="media/render-back.png" alt="Rear render of ChamberFlux V2" width="47%">
</p>

> [Download the printable files on Printables](PRINTABLES_LINK_HERE)

---

## About ChamberFlux

ChamberFlux is a compact, low-complexity chamber-circulation module created to improve air transport inside enclosed 3D printers and help existing filtration systems operate more effectively.

It is designed to integrate with the filter already installed in your printer rather than replace it. The module uses two high-airflow axial fans to move air through regions that may otherwise remain stagnant or poorly connected to the filter intake.

ChamberFlux:

* improves air transport toward an existing filter;
* reducing stagnant air regions;
* supports low speed mixing;
* maintains even chamber temperature 

The design uses common 40 mm fans and minimal hardware. It supports several mounting methods, multiple pivot positions, different wiring setups, and both horizontal and vertical installation.

---

## Why This Exists

Common chamber filters must push air through restrictive media such as activated carbon, carbon pellets, foam, or HEPA elements. Doing this requires fans with sufficient static pressure.

That creates an unavoidable engineering tradeoff:

* dense filter media improves filtration capacity while increasing resistance;
* increased resistance reduces total airflow;
* reduced airflow limits the working range/capacity of filters;
* circulation can remain concentrated near the filter while further regions remain poorly mixed.

This effect can be especially important for smaller and more compact filter systems. A filter may only have the ability to process the air immediately surrounding its intake repeatedly while contaminants remain in the chamber air.

Adding more carbon increases adsorption capacity, but it does not automatically ensure that contaminated air reaches that carbon during the duration of a print. Ultimately, the efficiency of a filter depends not only on its fan strength and media capacity, but also whether it's filtering the right air in the first place.

ChamberFlux addresses this side of the problem, providing a robust solution to boost your existing setup.

The fans used in chamber circulation against very little resistance, allowing them to move a larger volume of chamber air. They are not intended to push air through filter media. Instead, they circulate chamber air toward the working region of the existing filter while helping to regulate chamber temperature as well.

It is intended to improve the frequency with which chamber air reaches the filter, increasing effective chamber-scale removal without requiring a second carbon cartridge or a complete filtration-system replacement.

---

## Testing Data

ChamberFlux was tested in a controlled enclosure using a Nevermore Micro filter under passive and actively recirculated conditions. The key result was that a 30 g carbon setup with the recirculation module yielded lower VOC levels than a setup using 60 g of carbon, showing that improving chamber airflow can be even more effective than higher carbon mass. 

<p align="center">
  <img src="media/figure2.png" alt="Passive carbon treatment results" width="31%">
  <img src="media/figure3.png" alt="Active recirculation results" width="31%">
  <img src="media/figure4.png" alt="Summary comparison metrics" width="31%">
</p>

<details> <summary><strong>View testing details</strong></summary>

<br>

Testing was conducted in an enclosed chamber with acrylic walls using a fixed hotend to remove confounding variables, and a Nevermore Micro V6 filter. 4028 fans from VoxelPLA were used for recirculation. Five conditions were tested with four trials each:

no carbon, no recirculation (Control baseline);
30 g carbon, no recirculation (Treatment control);
60 g carbon, no recirculation;
30 g carbon, active recirculation;
60 g carbon, active recirculation.

Two SGP41 metal-oxide VOC sensors were placed at different chamber locations to compare sensor response and spatial uniformity. A BME688 sensor was also used to monitor secondary gas-response and environmental trends. The SGP41 readings are SRAW ticks which are logarithmically scaled. Sensors were housed in embedded housings covered by size 40 stainless steel mesh to reduce turbulence and ensure readings accurately reflected chamber conditions in active trials.

ABS filament was continuously extruded for 10 minutes at a rate of 5 mm/s for 900 s, followed by the opening of the chamber and a 300 s period of decay monitoring. Carbon in the filter was replaced with fresh carbon after each trial. 

</details>

---

## Hardware Features

### Compact dual-fan design

The assembled module has an approximate footprint of:

**107 × 52 × 44 mm**

This includes the mounting base, pivoting fan carrier, and two 40 mm axial fans. Note that this may be increased/reduced depending on the selected pivot slot and cover/fan configuration. 

The rear of the fan assembly maintains open clearance so that the fan inlets are not pressed directly against the mounting surface. 

### Universal mounting base

The mounting base supports several installation methods:

* M3 screws into T-slot extrusion hardware;
* integrated zip-tie mounting points;
* dedicated VHB mounting surface;
* optional press-fit magnet mounting;
* horizontal mounting;
* vertical mounting;
* inverted mounting.

### Adjustable pivoting fan carrier

The fan carrier can be aimed to suit the enclosure layout.

Features include:

* four available pivot mounting positions;
* M3 screw-joint adjustment;
* captive M3 hex-nut version;
* M3 heat-set-insert version;
* adjustable fan angle;
* compatibility with several mounting orientations;
* optional front fan cover.

The multiple pivot positions allow the user to prioritize clearance, wiring access, mounting orientation, or airflow direction.

### Flexible wiring

ChamberFlux includes:

* left- or right-side wiring exits;
* integrated wire channels;
* printed wire guides;
* strain-relief and zip-tie points;
* optional locking mounts for WAGO 221-2401 connectors.

The WAGO system is optional. The fans may be connected using any correctly rated and insulated wiring method.

### High-airflow axial fans

The circulation system is designed around 40 mm axial fans that provide high unrestricted airflow. This makes them appropriate for bulk chamber circulation because there is not any resistance the fan has to push through.

<p align="center">
  <img src="media/prototype-front.jpg" alt="ChamberFlux mounted to aluminum extrusion" width="47%">
  <img src="media/prototype-side.jpg" alt="ChamberFlux pivoted on aluminum extrusion" width="47%">
</p>

---

## Parts/BOM

### Printed parts

The entire assembly is simple and compact, requiring only 2 prints for a functional module. 

The only printed parts are the universal base plate, pivoting fan mount (Hex nut and heat-set insert version), and optional fan cover (Normal and low-profile version). 

> [Download ChamberFlux V2 on Printables](PRINTABLES_LINK_HERE)

### Required hardware

| Part                     | Quantity | Notes                                                                       |
| ------------------------ | -------: | --------------------------------------------------------------------------- |
| 40xx axial fans          |        2 | 4010, 4020, 4028, or another compatible 40 mm fan                           |
| M3×6 mm or longer screws |        4 | Used for pivot/base attachment; exact length depends on configuration       |
| M3 hex nuts              |        2 | Required for the hex-nut pivot version                                      |
| M3 heat-set inserts      |        2 | Used instead of hex nuts for the heat-set version                           |
| M3 fan screws            |        4 | Length depends on fan model and whether the optional cover is installed |

For 4028 fans with the optional front cover, use approximately:

**M3×35 mm or longer**

Always verify the required screw length against the specific fan model before assembly.

### Optional hardware

| Part                     |  Quantity | Purpose                      |
| ------------------------ | --------: | ---------------------------- |
| WAGO 221-2401 connectors |         2 | Clean removable fan wiring   |
| VHB tape                 | As needed | Panel mounting               |
| Zip ties                 | As needed | Mounting and wire management |
| M3 T-slot nuts           | As needed | Aluminum-extrusion mounting  |

### Suggested high-airflow fans

Any compatible 40 mm fan may be used. Fans already available from other printer projects may work.

Examples of dedicated high-airflow 4028 options include:

* [Voxel PLA 4028 High-Flow Fan Upgrades](https://voxelpla.com/products/4028-high-flow-fans-upgrades)
* [Delta FFB0412SHN 4028 Axial Fan](https://central3dprinting.com/products/delta-4028-12v-0-6a-axial-fan-ffb0412shn-2-pin-4-pin-pwm)

These links are examples only and are not sponsorships/required parts.

---

## Assembly Instructions

### Step 1 — Install the fans and optional cover

Place both fans into the pivoting fan carrier.

If using the optional front cover:

1. Insert the four M3 screws through the front cover.
2. Align the screws with the fan mounting holes.
3. Thread the screws into the printed fan carrier.
4. Tighten only until the assembly is secure.

Do not overtighten the screws or crush the fan frames.

<p align="center">
  <img src="media/AssemblyStep1.png" alt="Installing fans and optional cover" width="90%">
</p>

### Step 2 — Install the pivot hardware

1. Insert an M3 hex nut into each captive nut pocket, or install the M3 heat-set inserts.
2. Select the preferred pivot mounting position.
3. Align the fan carrier with the selected holes.
4. Insert the M3 screws.
5. Tighten the screws until the selected angle is held securely.

<p align="center">
  <img src="media/AssemblyStep2.png" alt="Installing the pivoting fan carrier" width="90%">
</p>

### Step 3 — Route and connect the wiring

1. Choose the left or right wiring exit.
2. Route the fan leads through the integrated wire guides.
3. Connect the fan leads using the desired wiring method.
4. If using WAGO 221-2401 connectors, attach both sides of the wiring before sliding the connectors into the locking mounts.
5. Connect the assembly to a correctly rated power source or printer-board output.

<p align="center">
  <img src="media/AssemblyStep3.png" alt="Routing and connecting the fan wiring" width="90%">
</p>

---

## Installation and Compatibility

ChamberFlux is intended for enclosed FDM printers with existing filtration module systems. It is designed to have a profile and mounting system compatible with most available commercial and DIY printers.

### Recommended placement

Good starting locations include:

* a rear corner;
* an edge near the bottom of the chamber
* a side wall opposite the existing filter;
* a region that remains poorly mixed;

The pivoting carrier can be aimed:

* across the upper chamber;
* along a wall;
* toward the intake region of the existing filter;

In printers without extrusion-based frames, the built in adhesive patches can be used with VHB tape/any other adhesive, or the zip tie slots can be used to attach to the existing structure.

<p align="center">
  <img src="media/installed-bambu.jpg" alt="ChamberFlux installed inside an enclosed printer" width="47%">
  <img src="media/cad-installation.png" alt="ChamberFlux installed in an extrusion-frame enclosure" width="47%">
</p>

---

## License

Licensed under GNU General Public License v3.0.

---

