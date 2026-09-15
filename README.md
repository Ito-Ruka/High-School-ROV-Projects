# High-Current ESC Carrier & Power Distribution Board

<p align="center">
  <img src="Images/ESC Holder (Top view).png" alt="ESC Holder Board Top View" width="850">
</p>

<p align="center">
  <em>A dedicated power distribution and signal routing carrier designed for Blue Robotics Basic ESCs driving T200 Thrusters.</em>
</p>

---

### Overview

This carrier board consolidates discrete motor controllers into an integrated, serviceable module inside tight electronics enclosures. It pairs high-current DC bus routing with low-noise signal channels to eliminate wire harness congestion and streamline thruster maintenance.

* **Primary Application:** Power distribution and PWM signal breakout for up to 6 external ESCs
* **Target Hardware:** Blue Robotics Basic ESC / T200 Thruster systems
* **Design Toolchain:** KiCad 10.0 Native

---

### Key Architectural Features

* **Integrated ESC Mounting:** Mechanically aligns and retains up to 6 discrete ESC modules into a rigid, compact frame.
* **Optimized Thermal Spreading:** Heavy copper planes provide massive thermal mass and heat dissipation across the substrate during sustained loads.
* **Clean Harness Management:** Groups power taps and signal headers to decouple propulsion wiring from sensitive telemetry lines.
* **Dedicated Auxiliary Port:** Supplies clean parallel DC power for onboard sensors, logic, or auxiliary payloads.

---

### Visual Reference

<table>
  <tr>
    <td width="50%" align="center">
      <img src="Images/ESC Holder (Top view).png" alt="Top-down 2D trace routing view" width="100%" />
      <br><strong>Top Layer & Component Layout</strong>
    </td>
    <td width="50%" align="center">
      <img src="Images/ESC Holder (Back View).png" alt="Back view ground plane and routing" width="100%" />
      <br><strong>Bottom Layer & Ground Plane</strong>
    </td>
  </tr>
</table>

---

### Electrical & Mechanical Specifications

| Parameter | Specification | Design Notes |
| :--- | :--- | :--- |
| **Operating Voltage** | 12 V DC | Nominal battery bus input |
| **Max Continuous Current** | 20 A total | Sized for sustained multi-thruster runs |
| **Per-Channel Allocation** | 3 A per ESC channel | Dedicated rail routing for 6 ESC positions |
| **Auxiliary Power Rail** | 2 A continuous capacity | Dedicated breakout for accessories/sensors |
| **Board Dimensions** | 159 mm × 128 mm × 1.6 mm | Landscape $(W \times H \times T)$ footprint |
| **Layer Count** | 2-Layer FR4 | Standard fab; aluminum backing compatible |
| **Copper Weight** | 15 oz/ft² ($525\ \mu\text{m}$) | Extreme heavy copper power distribution |

---

### Fabrication & Assembly Notes (15 oz Copper)
* **Etch Clearance:** Minimum trace clearance and spacing set to $\ge 1.2\text{ mm}$ ($50\text{ mil}$) to prevent shorts from chemical undercut during $525\ \mu\text{m}$ copper etching.
