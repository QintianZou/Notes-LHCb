# PKU Group Meeting
Tuesday Sep 29, 2026, 6:00 PM → 8:00 PM 
Yuanning Gao (Peking University (CN)), 
Yanxi Zhang (Peking University (CN)), 
Zhenwei Yang (Peking University (CN)), 
Liupan An (Peking University (CN))

# Technical Highlights

# LHCb CALO RP Surveys 

## 1. Overview

**CALO RP Surveys** refers to **Radiation Protection (RP) surveys performed around the LHCb Calorimeter System (CALO)**.

In simple terms:

> **CALO RP Survey = measuring and assessing radiation levels around the calorimeter area before or during detector interventions.**

The main purpose is to ensure that personnel can safely access the CALO area for:

* maintenance
* inspection
* detector replacement
* installation
* upgrade activities
* cable and electronics work
* mechanical interventions

A simplified interpretation is:

$$
\text{CALO RP Survey}
=
\text{Radiation measurement}
+
$$

$$
\text{Access assessment}
+
\text{Work planning}
$$

---

# 2. What does CALO mean?

**CALO** is the LHCb **Calorimeter System**.

The calorimeter system is mainly responsible for measuring particle energy and identifying electromagnetic and hadronic activity.

The main calorimeter components include:

* **ECAL — Electromagnetic Calorimeter**
* **HCAL — Hadronic Calorimeter**

In older LHCb configurations, the CALO system also included:

* **SPD — Scintillating Pad Detector**
* **PS — Preshower Detector**

The SPD and PS were removed as part of the Upgrade I detector configuration.

---

# 3. What does RP mean?

**RP = Radiation Protection.**

Radiation Protection is concerned with protecting personnel from ionizing radiation produced by accelerator and detector operations.

During LHC operation, particles produced in proton-proton collisions can interact with detector materials.

After prolonged irradiation(放射，辐照), some detector materials can become activated:

$$
\text{Particle irradiation}
\rightarrow
\text{Nuclear activation}
\rightarrow
\text{Residual radioactivity}
$$

Therefore, even after the LHC beam has been stopped, some detector components may remain radioactive for a period of time.

This is known as:

> **Residual radiation / residual dose rate**

---

# 4. Why are CALO RP Surveys necessary?

During normal operation, personnel generally cannot freely access detector areas close to the beam line.

After beam operation stops, maintenance and upgrade work becomes possible during a **Long Shutdown (LS)**.

However, the radiation conditions must first be assessed.

A simplified sequence is:

```text
LHC operation
      ↓
Beam stops
      ↓
Cool-down / radioactive decay
      ↓
RP Survey
      ↓
Radiation levels assessed
      ↓
Access conditions determined
      ↓
Maintenance / upgrade work
```

Therefore:

$$
\boxed{
\text{RP Survey}
\rightarrow
\text{safe access planning}
}
$$

---

# 5. What is measured during an RP Survey?

A radiation protection survey can involve measurements such as:

## 5.1 Dose rate

One of the most important quantities is the **dose rate**.

Typical units include:

$$
\mu\text{Sv/h}
$$

or

$$
\text{mSv/h}
$$

The measured dose rate can vary significantly depending on:

* detector location
* distance from activated components
* irradiation history
* material composition
* beam conditions
* cooling time after beam operation

---

## 5.2 Spatial radiation distribution

Measurements can be taken at multiple locations around the detector.

This allows an approximate radiation map to be constructed:

```text
             CALO

       Low       Medium       High
        ↓          ↓           ↓

      [  ]       [  ]        [██]
      [  ]       [██]        [██]
      [  ]       [██]        [██]
```

Such information can help identify:

* high-dose areas
* lower-dose work areas
* access routes
* locations requiring additional shielding

---


# 7. Why can calorimeters become activated?

CALO contains substantial amounts of material, including absorber and structural materials.

Particles produced in collisions can interact with these materials.

For example:

$$
n + \text{nucleus}
\rightarrow
\text{activated nucleus}
$$

The resulting radioactive isotopes can decay later and produce radiation.

The level of activation depends on many factors, including:

* integrated beam exposure
* particle flux
* material composition
* geometry
* location relative to the interaction region
* time since beam operation stopped

Therefore, different parts of CALO can have different radiation levels.

---


# 11. ALARA Principle

Radiation protection activities commonly follow the principle of:

> **ALARA — As Low As Reasonably Achievable**

The objective is to keep radiation exposure as low as reasonably achievable while carrying out necessary work.

In practical detector work, this can mean:

```text
Reduce exposure time
        +
Increase distance
        +
Use shielding
        +
Optimize work sequence
```
WDP = Work Dose Planning，工作剂量规划
---
# UT Opening Preparation

UT opening preparation
• Warm up
• CO2 pipes disconnection A & C sides
## 2. UT Opening Preparation

**UT opening preparation** means preparing the UT for physical access, maintenance, removal, or installation work.

A key part of this preparation is the cooling-system intervention.

---

## 3. Warm Up

The UT operates with a low-temperature CO₂ cooling system.

Before opening the detector:

```text
Normal operation
      ↓
Controlled warm-up
      ↓
Safe temperature
      ↓
CO₂ system isolation
```

**Warm up** means bringing the detector and cooling system from operating temperature to a suitable temperature for maintenance.

---

## 4. CO₂ Pipes Disconnection

The UT cooling system uses **CO₂ evaporative cooling**.

Before the UT can be opened, the relevant CO₂ circuits must be safely isolated and disconnected.

```text
CO₂ cooling system
        ↓
   UT cooling
        ↓
  Warm-up / isolation
        ↓
CO₂ pipe disconnection
        ↓
     UT opening
```

---

## 5. A & C Sides

**A side** and **C side** refer to the two sides of the UT/detector system.

Therefore:

> **CO₂ pipes disconnection A & C sides**

means that the CO₂ cooling connections on **both the A side and C side** need to be disconnected.

---
# Why Silicon Detectors Use CO₂ Cooling

## 1. Why does a silicon detector need cooling?

Silicon detectors are exposed to a large amount of radiation during LHC operation.

Radiation creates defects in the silicon crystal lattice. These defects increase the detector **leakage current**:

$$
\text{Radiation}
\rightarrow
\text{Silicon damage}
\rightarrow
\text{Higher leakage current}
$$

The leakage current increases with temperature.

Therefore, operating the detector at a low temperature helps reduce leakage current and slows down the effects of radiation damage.

A simplified relationship is:

$$
I_{\mathrm{leak}} \propto T^2 e^{-E_g/(2kT)}
$$

where:

* \(I_{\mathrm{leak}}\) = leakage current
* \(T\) = detector temperature
* \(E_g\) = silicon band-gap energy
* \(k\) = Boltzmann constant

The important point is:

> **Lower temperature → lower leakage current → better detector performance and lower power dissipation.**


The UT is close to the proton-proton collision point and receives a significant radiation dose.

Therefore, the detector must operate under conditions that limit radiation-induced degradation.


---

## 2. Why use CO₂?

LHCb uses **evaporative CO₂ cooling** for silicon detector systems.

The basic principle is:

```text
Liquid CO₂
    ↓
High-pressure cooling circuit
    ↓
CO₂ evaporates
    ↓
Heat is absorbed
    ↓
Detector is cooled
```

The key physical mechanism is the **latent heat of vaporization**.


---
# Beam Pipe Venting — Summary

## Preparation for Beam Pipe Removal

### Beam Pipe Venting (TE-VSC)

A major work package carried out by **TE-VSC** to prepare the beam pipe for removal.

The beam pipe normally operates under **ultra-high vacuum (UHV)**. Before it can be opened or removed, the vacuum must be safely and controllably broken (**venting**).

#### Main Activities

* **GIS Table bake-out installation and commissioning**

  * **Bake-out** means heating vacuum components to remove adsorbed gases and moisture from their surfaces.
  * This reduces **outgassing** and helps maintain good vacuum conditions.
  * *Commissioning* means testing and verifying that the installed system operates correctly.

* **Neon venting**

  * **Venting** means controlled filling of the vacuum system with a gas.
  * In this procedure, **neon (Ne)** is used as the venting gas rather than simply exposing the beam pipe to air.
  * The controlled venting brings the beam pipe from vacuum conditions to a state suitable for subsequent removal work.
# HCAL PMT and Shielding Wall 

## HCAL PMT 

**HCAL (Hadronic Calorimeter)** measures the energy deposited by hadrons.

**PMT (Photomultiplier Tube)** is part of the HCAL readout system. It converts weak scintillation light into an electrical signal and amplifies it.

```text
Hadron
  ↓
HCAL scintillator
  ↓
Scintillation light
  ↓
PMT
  ↓
Electrical signal
  ↓
Energy measurement
```

**Key point:**
The **PMT is a readout device**, not the main energy-absorbing part of the calorimeter. It detects and amplifies the light produced by the scintillator.

---

## Shielding Wall → Radiation Protection Structure

A **shielding wall** is a thick structure made of radiation-attenuating material, such as steel or concrete, used to reduce radiation levels in surrounding areas.

```text
Radiation source
      ↓
████████████
 Shielding wall
████████████
      ↓
Lower radiation level
      ↓
Accessible/work area
```

Its main purposes are to:

* **Attenuate radiation** reaching surrounding areas.
* **Protect personnel and equipment**.
* Help define controlled and accessible areas during operation and maintenance.

