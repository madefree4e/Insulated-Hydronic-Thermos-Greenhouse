# Insulated Hydronic "Thermos" Greenhouse (V1.0)
**A Zero-Grid, R-30 Year-Round Food Production System for Sub-Zero Climates**

## Overview
Traditional greenhouses lose up to 90% of their heat through clear glass or polycarbonate glazing ($R\text{-1.5}$ rating). The **Insulated Hydronic "Thermos" Greenhouse** flips this paradigm by replacing transparent walls with a high-performance $R\text{-30}$ insulated building envelope and piping sunlight directly into the interior using high-efficiency Tubular Daylighting Devices (TDDs). 

To prevent daytime overheating and survive freezing nights (down to $-15^\circ\text{F} / -26^\circ\text{C}$), the system integrates an active hydronic thermal battery beneath elevated plant beds. The entire climate control loop is governed by a pure analog bimetallic relay circuit—requiring **zero microcontrollers, zero software, and ultra-low electrical power**.

---

## 1. System Architecture & Layout

                    [ Direct Sunlight ]
                            |
               +------------v------------+
               |  Tubular Light Pipes    |  <-- 99.7% Spectral Reflectance
               +------------+------------+
                            |
  +-------------------------v-------------------------+
  |  R-30 Insulated Roof & Envelope (SIPs or 2x6)      |
  |                                                   |
  |       [ Radiator / Fan Dehumidifier Assembly ]    |  <-- Ceiling Heat Capture
  |                        |                          |
  |        +---------------v---------------+          |
  |        | Elevated Crop Growing Benches |          |  <-- Root Zone Warming
  |        +---------------+---------------+          |
  |                        |                          |
  |        [ 300-Gal Water Thermal Battery ]          |  <-- Placed in Dead Space
  |                                                   |
  +---------------------------------------------------+


### 1.1 Building Envelope Specifications
* **Wall & Roof Construction:** Structural Insulated Panels (SIPs) or $2\times 6$ framing with closed-cell spray foam / rigid polyisocyanurate insulation.
* **Thermal Resistance:** Minimum $R\text{-20}$ walls, $R\text{-30}$ roof/ceiling.
* **Vapor Barrier:** Continuous interior polyethylene vapor barrier to protect insulation from high-humidity crop environments.
* **Exterior Dimensions (Baseline Model):** $12\text{ ft} \times 16\text{ ft} \times 8\text{ ft}$ ceiling ($\approx 1,536\text{ cu ft}$ internal air volume).

---

## 2. Light Ingestion & Daylighting Optics

Instead of transparent walls, light is ingested through ceiling-mounted light conduits:
* **Collector Domes:** $4\times 14\text{-inch}$ roof-mounted acrylic domes equipped with internal Fresnel reflectors to capture low-angle winter sunlight.
* **Conduits:** Rigid aluminum light tubes lined with multi-layer silver film providing **99.7% spectral reflectance**.
* **Diffusion:** Ceiling diffusers spread Photosynthetically Active Radiation (PAR) uniformly across the crop canopy without creating harsh hotspots.
* **Thermal Gain:** Ingested PAR light strikes plants and floor surfaces, converting directly into trapped infrared heat inside the $R\text{-30}$ thermos shell.

---

## 3. Hydronic Thermal Battery & Heat Exchanger

To store daytime solar-thermal energy for nighttime heating, an active hydronic loop transfers energy from the hot ceiling air into a water storage mass located beneath the crop beds.

[ Ceiling Air (80°F+) ] ---> [ 12V Fan ] ---> [ Aluminum Radiator ] ---> [ Cool
Air (60°F) ] | (12V Water Pump) | v [ Under-Bed Water Storage ]


### 3.1 Water Storage Matrix
* **Capacity:** 300 Gallons ($\approx 2,500\text{ lbs}$) of water distributed across plastic food-grade tanks or drums.
* **Placement:** Positioned directly inside the dead space beneath elevated growing benches.
* **Secondary Benefit (Root-Zone Warming):** As the water battery holds heat at night, thermal energy passively radiates upward through the bench floors, keeping plant soil at an optimal $60^\circ\text{F}\text{--}65^\circ\text{F}$ even if air temperatures drop.

### 3.2 Active Heat Exchanger & Dehumidification
* **Radiator Unit:** 12V Heavy-Duty Aluminum Automotive Heater Core / Hydronic Coil ($12\text{"} \times 12\text{"}$).
* **Air Prime Mover:** 12V Brushless DC High-CFM Duct Fan ($150\text{--}200\text{ CFM}$).
* **Fluid Prime Mover:** 12V Brushless Submersible/Inline Water Pump ($2.5\text{ GPM}$).
* **Automated Condensate Recovery:** As warm, humid greenhouse air is drawn across the cooler radiator coils, water vapor condenses. A drip pan under the coil collects distilled water runoff for crop irrigation, automatically regulating daytime humidity.

---

## 4. Pure Analog Electrical & Control Logic

The system eliminates microcontrollers, software, and fragile sensors. All operations are handled via a **12V DC power system** driven by a small solar panel, battery, and bimetallic snap/spring switches.

+12V Battery Bus | +--- [ High-Temp Snap Switch (>75°F Ceiling) ] ----+--->
(Daytime Charge Loop) | | Pumps Heat into Water | | +--- [ Bimetallic Thermostat
(<42°F Room) ] -------+---> [ 12V Relay Coil ] | +---> (Nighttime Heating Loop)
Pumps Heat OUT of Water


### 4.1 Dual Operational Modes

1. **Daytime Heat Harvesting Mode (Charge):**
   * A surface-mount bimetallic high-temp snap switch ($75^\circ\text{F}$ NO) is mounted near the ceiling light pipes.
   * When ceiling air hits $75^\circ\text{F}$, the switch closes, powering the 12V fan and pump. Warm air is pulled through the radiator, heating the 300-gallon water battery.

2. **Nighttime Hydronic Heating Mode (Discharge):**
   * An analog bimetallic wall thermostat (set to $42^\circ\text{F}$) monitors room temperature.
   * When room air drops below $42^\circ\text{F}$, the thermostat mechanically closes, tripping a standard 12V automotive relay.
   * The relay powers the pump and fan from the 12V battery, circulating $80^\circ\text{F}$ water back through the radiator to blow warm air directly into the greenhouse.

---

## 5. Thermodynamic Performance Baseline

Calculated for a $12\text{ ft} \times 16\text{ ft} \times 8\text{ ft}$ insulated structure operating in sub-zero winter conditions (Outdoor: $-15^\circ\text{F}$, Interior Target: $45^\circ\text{F}$).

* **Building Heat Loss Rate:** $\approx 1,850\text{ BTUh}$ at $-15^\circ\text{F}$ outdoor ambient temperature ($R\text{-20/R-30}$ envelope).
* **Thermal Battery Storage Capacity:**
  $$\text{Capacity} = 2,500\text{ lbs Water} \times 1\text{ BTU/lb}^\circ\text{F} \times 25^\circ\text{F } \Delta T = \mathbf{62,500\text{ BTUs}}$$
* **Autonomous Freeze Float Duration (Zero Sun):**
  $$\text{Float Time} = \frac{62,500\text{ BTUs}}{1,850\text{ BTUh}} = \mathbf{\approx 33.7\text{ Hours}}$$
* **Parasitic Electrical Draw:**
  * Active Heating/Charging State: $\approx 18\text{ Watts}$ ($1.5\text{ Amps}$ at $12\text{V DC}$).
  * Standby State: **0.0 Watts** (No microcontrollers or digital draws).

---

## 6. Bill of Materials (BOM) & Estimated Costs

| Component | Specification / Description | Qty | Est. Cost (USD) |
| :--- | :--- | :--- | :--- |
| **Light Pipes** | 14" Tubular Daylighting Devices (TDDs) | 4 | $600.00 |
| **Water Tanks** | 55-Gallon Heavy Duty HDPE Water Drums | 6 | $240.00 |
| **Radiator** | Aluminum Automotive Heater Core / Hydronic Coil | 1 | $35.00 |
| **Water Pump** | 12V DC Brushless Solar/Hydronic Pump (2.5 GPM) | 1 | $20.00 |
| **Air Fan** | 12V DC High-CFM Inline Duct Fan | 1 | $25.00 |
| **Thermostat** | Classic Bimetallic Spring Wall Thermostat | 1 | $15.00 |
| **Snap Switch** | 75°F Normally Open (NO) Thermal Snap Disc | 1 | $8.00 |
| **Relay** | 12V 40A Automotive Relay + Harness | 1 | $7.00 |
| **Solar Power** | 50W Solar Panel + 12V 20Ah LiFePO4 Battery | 1 | $110.00 |
| **Piping & Hardware**| 3/4" PEX tubing, fittings, drip tray, wire | -- | $80.00 |
| **TOTAL (Excl. Framing)** | | | **~$1,140.00** |

---

## 7. License & Open Source Contribution
This specification is released under the **CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S)**. 

Feel free to fork, adapt, build, and submit Pull Requests to improve the thermal modeling, CAD drawings, or material sourcing options!
