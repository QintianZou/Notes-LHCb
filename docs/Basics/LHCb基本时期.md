# LHCb Upgrade I, Upgrade II, and LHC Long Shutdowns

## 1. Overview

To cope with increasing collision rates and luminosity at the LHC, the LHCb detector has undergone major upgrade programs.

The key concepts are:

* **Run**: a period during which the LHC is operating and collecting physics data.
* **LS (Long Shutdown)**: a long period when the LHC is stopped for maintenance, consolidation, and upgrades.
* **Upgrade I**: the major LHCb upgrade installed mainly during LS2.
* **Upgrade II**: the next major LHCb upgrade, planned to be installed during LS4.
* **LS3**: an important transition period during which LHCb will further enhance Upgrade I and prepare technologies for Upgrade II.

A simplified picture is:

```text
Run 1 → LS1 → Run 2 → LS2 → Run 3 → LS3 → Run 4 → LS4 → Run 5/6
                         │            │            │
                         ▼            ▼            ▼
                     Upgrade I      Upgrade I    Upgrade II
                    installation   enhancement   installation
```

---

# 2. LHC Runs and Long Shutdowns

## 2.1 Run 1

**Run 1:** approximately 2010–2012

During Run 1, LHCb operated with the original detector configuration.

The experiment collected data primarily for:

* CP violation measurements
* $B$-meson physics
* Rare decays
* Charm physics
* Heavy-flavour spectroscopy

After Run 1, the LHC entered its first major long shutdown.

---

## 2.2 LS1 — Long Shutdown 1

**LS1:** approximately 2013–2014

LS1 was the first major long shutdown of the LHC.

The main purposes were:

* Accelerator maintenance and consolidation
* Improvements to LHC infrastructure
* Upgrades to the LHC experiments
* Preparation for the higher-energy and higher-performance Run 2

LHCb also performed detector improvements during this period.

After LS1, the LHC entered Run 2.

---

## 2.3 Run 2

**Run 2:** approximately 2015–2018

LHCb continued physics data taking with the upgraded Run-2 configuration.

However, the limitations of the original detector architecture became increasingly important as the LHC luminosity and collision rate increased.

In particular:

* The detector readout rate was limited.
* Hardware-based trigger systems limited the amount of information that could be retained.
* The detector was not designed for the much higher data rates expected in future LHC running.

These limitations motivated the much more extensive **LHCb Upgrade I**.

---

# 3. LS2 and LHCb Upgrade I

## 3.1 LS2 — Long Shutdown 2

**LS2:** approximately 2019–2022

LS2 was a major milestone for LHCb.

During LS2, most of the original LHCb detector was removed or substantially modified, and a new detector architecture was installed.

The main objective was to prepare LHCb for **Run 3** and higher instantaneous luminosity.

The relationship can be summarized as:

```text
LS2
 │
 └──→ Major installation of LHCb Upgrade I
          │
          └──→ Run 3
```

---

# 4. LHCb Upgrade I

## 4.1 Main Motivation

The central motivation for Upgrade I was to allow LHCb to operate efficiently at much higher collision rates.

One of the most important changes was the move toward a **40 MHz readout architecture and a fully software-based trigger strategy**.

Instead of relying primarily on hardware triggers to reject events at an early stage, the upgraded LHCb can read out detector information at the LHC bunch-crossing frequency and use real-time computing to select interesting events.

This requires:

* High-speed detector electronics
* High-bandwidth data transmission
* Large-scale real-time computing
* GPU and CPU resources
* Sophisticated reconstruction and event-selection algorithms

The Upgrade I design targets an instantaneous luminosity of approximately

$$
\mathcal{L} \sim 2 \times 10^{33}\ \mathrm{cm}^{-2}\mathrm{s}^{-1}
$$

and an integrated luminosity of roughly

$$
\mathcal{L}_{\mathrm{int}} \sim 50\ \mathrm{fb}^{-1}.
$$

---

# 5. Major Detector Components in Upgrade I

Upgrade I involved major changes to almost all major detector subsystems.

## 5.1 VELO — Vertex Locator

The **VELO** is located very close to the proton-proton interaction point.

Its primary purposes are:

* Precise reconstruction of primary vertices
* Precise reconstruction of secondary vertices
* Identification of displaced heavy-flavour decays
* Measurement of particle trajectories close to the interaction point

Upgrade I introduced a new **pixel-based VELO**.

The high spatial resolution of the pixel detector is particularly important for reconstructing $b$- and $c$-hadron decays.

---

## 5.2 UT — Upstream Tracker

The **Upstream Tracker (UT)** is located upstream of the dipole magnet.

Its main functions include:

* Charged-particle tracking
* Providing tracking information before the magnetic field
* Improving momentum reconstruction when combined with downstream tracking detectors

Upgrade I introduced a new silicon-strip-based tracking system.

---

## 5.3 SciFi Tracker

The **Scintillating Fibre Tracker (SciFi)** is located downstream of the dipole magnet.

It uses scintillating fibres to reconstruct charged-particle trajectories.

Its position can be summarized as:

```text
Interaction Point
       │
       ▼
     VELO
       │
       ▼
      UT
       │
       ▼
   Dipole Magnet
       │
       ▼
     SciFi
```

The combination of VELO, UT, and SciFi provides high-quality charged-particle tracking.

---

## 5.4 RICH — Ring Imaging Cherenkov Detectors

The **RICH detectors** provide particle identification (PID), particularly for distinguishing particles such as:

* $\pi$
* $K$
* $p$

Particle identification is essential for many LHCb analyses.

For example, distinguishing kaons from pions is critical in many $B$-meson decay measurements.

Upgrade I introduced new detector components and faster readout electronics to cope with the increased data rate.

---

## 5.5 Calorimeters

The LHCb calorimeter system measures the energy of particles, particularly electrons, photons, and hadrons.

Upgrade I included improvements to the calorimeter readout and electronics to accommodate the new operating conditions.

Further calorimeter improvements are planned during LS3.

---

## 5.6 Muon System

The muon system identifies muons and provides tracking information relevant to muon-based physics channels.

Upgrade I included improvements to:

* Electronics
* Readout
* Detector operation
* Radiation and background tolerance

---

# 6. Run 3

**Run 3:** approximately 2022–2025

After LS2, LHCb began Run 3 with the Upgrade I detector.

A major milestone was the start of proton-proton collision data taking with the upgraded detector in 2022.

The key characteristics of Run 3 include:

* Fully upgraded detector
* 40 MHz readout architecture
* Software-based trigger
* Real-time event reconstruction
* GPU/CPU-based computing
* Higher instantaneous luminosity than the previous LHCb configuration

This marks a fundamental change in the way LHCb collects and processes data.

---

# 7. LS3 — Long Shutdown 3

## 7.1 What is LS3?

**LS3 = Long Shutdown 3.**

LS3 is the next major long shutdown of the LHC and is planned for approximately **2026–2028**, although the detailed accelerator schedule can evolve.

LS3 is particularly important for LHCb because it serves as a transition between Upgrade I and the future Upgrade II program.

A simplified picture is:

```text
Upgrade I
    │
    ▼
  Run 3
    │
    ▼
   LS3
    │
    ├── Upgrade I enhancements
    ├── ECAL improvements
    ├── RICH electronics improvements
    ├── Online/DAQ improvements
    └── Preparation for Upgrade II
    │
    ▼
  Run 4
    │
    ▼
   LS4
    │
    ▼
Upgrade II
```

## 7.2 LS3 Is Not the Main Upgrade II Installation

An important distinction is:

> **LS3 is not the main installation period for Upgrade II.**

Instead, LS3 includes targeted detector enhancements and technology preparation.

Examples include:

* ECAL improvements
* RICH electronics upgrades
* Improvements to online processing and data acquisition
* Preparatory work for future Upgrade II detector technologies

For example, the ECAL inner region is planned to benefit from new technologies such as the **SpaCal (Spaghetti Calorimeter)** concept.

The RICH system will also receive further improvements to its electronics and readout capabilities.

---

# 8. Upgrade II

## 8.1 Motivation

Upgrade II is the next major LHCb detector upgrade.

The primary motivation is the much more demanding environment expected at the **High-Luminosity LHC (HL-LHC)**.

Compared with Upgrade I, Upgrade II is designed for:

* Much higher collision rates
* Higher instantaneous luminosity
* Higher detector occupancy
* Larger radiation doses
* Much higher data rates
* More challenging pile-up conditions

The overall goal is to enable LHCb to collect a much larger data sample while maintaining excellent tracking, particle identification, timing, and trigger performance.

---

# 9. Upgrade II Physics Program

Upgrade II is designed around a very large integrated luminosity target.

The current planning target is approximately:

$$
\boxed{\mathcal{L}_{\mathrm{int}} \sim 300\ \mathrm{fb}^{-1}}
$$

This is substantially larger than the approximately

$$
\sim 50\ \mathrm{fb}^{-1}
$$

target associated with Upgrade I.

The increased data sample will significantly improve the statistical precision of measurements in heavy-flavour physics.

Important physics topics include:

* CP violation
* Rare $B$ decays
* Rare charm decays
* CKM measurements
* Lepton-flavour universality tests
* Heavy-flavour spectroscopy
* Searches for indirect signatures of New Physics

---

# 10. Why Upgrade II Requires New Detector Technologies

The HL-LHC environment introduces several major challenges.

As the luminosity increases:

$$
\text{Collision Rate} \uparrow
$$

which leads to:

$$
\text{Occupancy} \uparrow
$$

$$
\text{Radiation Dose} \uparrow
$$

$$
\text{Data Rate} \uparrow
$$

Therefore, the detector needs to become:

* Faster
* More radiation tolerant
* More granular
* More capable of precision timing
* More capable of handling high data throughput

---

# 11. 4D Tracking and Timing

One of the important concepts for Upgrade II is **4D tracking**.

Traditional tracking primarily measures spatial information:

$$
x,\ y,\ z
$$

Upgrade II increasingly aims to include precise timing information:

$$
x,\ y,\ z,\ t
$$

The additional time coordinate can help distinguish particles originating from different collisions occurring close together in space and time.

This becomes particularly important under high-pile-up conditions.

Thus, precision timing can provide another dimension for event reconstruction and background rejection.

---

# 12. Upgrade I vs. Upgrade II

| Feature                      | Upgrade I                                              | Upgrade II                                           |
| ---------------------------- | ------------------------------------------------------ | ---------------------------------------------------- |
| Main installation period     | LS2                                                    | LS4                                                  |
| Main physics runs            | Run 3 / Run 4                                          | Run 5 / Run 6                                        |
| Target luminosity            | $\sim 2\times10^{33}\ \mathrm{cm}^{-2}\mathrm{s}^{-1}$ | $\sim10^{34}\ \mathrm{cm}^{-2}\mathrm{s}^{-1}$ scale |
| Integrated luminosity target | $\sim50\ \mathrm{fb}^{-1}$                             | $\sim300\ \mathrm{fb}^{-1}$                          |
| Readout                      | 40 MHz                                                 | Higher-rate architecture                             |
| Trigger                      | Software-based                                         | More advanced real-time processing                   |
| Tracking                     | Pixel VELO + UT + SciFi                                | Higher radiation tolerance, granularity, and timing  |
| RICH                         | Upgraded for Run 3                                     | Higher-rate and timing capabilities                  |
| Calorimeter                  | Upgrade I + LS3 improvements                           | New-generation detector technologies                 |
| Main challenge               | High-rate Run 3 environment                            | HL-LHC high-rate/high-radiation environment          |

The exact luminosity and schedule targets are subject to evolution as the LHC and LHCb programs develop.

---


# 14. The Big Picture

The evolution of LHCb can be summarized as a progression toward higher luminosity, higher data rates, and more precise measurements:

```text
                 LHCb Detector Evolution

 Original LHCb
     │
     │ Run 1 / Run 2
     ▼
    LS2
     │
     ▼
  Upgrade I
     │
     │ 40 MHz readout
     │ Software trigger
     │ New tracking
     │ New VELO
     │ New RICH electronics
     ▼
    Run 3
     │
     ▼
    LS3
     │
     │ ECAL enhancement
     │ RICH enhancement
     │ Online/DAQ improvements
     │ Upgrade II preparation
     ▼
    Run 4
     │
     ▼
    LS4
     │
     ▼
  Upgrade II
     │
     │ Higher luminosity
     │ Higher radiation tolerance
     │ Higher granularity
     │ Precision timing / 4D tracking
     │ Much larger data sample
     ▼
   Run 5 / Run 6
     │
     ▼
 ~300 fb⁻¹ physics program
```

---

# 15. Key Takeaways

The most important points to remember are:

1. **LS1, LS2, LS3, and LS4 are Long Shutdown periods of the LHC.**

2. **Upgrade I was mainly installed during LS2** and enabled LHCb's Run 3 detector architecture.

3. **Upgrade I introduced a fundamentally new readout and trigger concept**, based on 40 MHz readout and software-based real-time event selection.

4. **Run 3 is the first major physics run using the Upgrade I detector.**

5. **LS3 is a transition period rather than the main Upgrade II installation.** It includes targeted improvements to Upgrade I and preparation for Upgrade II.

6. **Upgrade II is planned to be installed mainly during LS4.**

7. **Upgrade II is designed for the much more demanding HL-LHC environment**, with higher luminosity, radiation, occupancy, and data rates.

8. **Precision timing becomes increasingly important for Upgrade II**, providing information that can be thought of as an additional time coordinate in particle reconstruction.

9. The overall progression is:

```text
Original LHCb
      ↓
     LS2
      ↓
  Upgrade I
      ↓
    Run 3
      ↓
     LS3
      ↓
  Enhanced Upgrade I
      ↓
    Run 4
      ↓
     LS4
      ↓
  Upgrade II
      ↓
   Run 5 / 6
```

---

