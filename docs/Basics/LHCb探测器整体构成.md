# Introduction to LHCb Detectors
# LHCb Tracking System 

## 1. What is the Tracking System?

The **Tracking System** reconstructs the trajectories of charged particles as they pass through the detector.

Its main goals are to determine:
- where a charged particle passed through the detector;
- the particle's trajectory and direction;
- its momentum;
- the sign of its electric charge.

A simplified reconstruction chain is:

$$
\text{Particle}
\rightarrow
\text{Hits}
\rightarrow
\text{Track}
\rightarrow
\text{Curvature}
\rightarrow
(p,q)
$$

The Tracking System is mainly sensitive to charged particles such as

$$
\pi^\pm,\quad K^\pm,\quad p,\quad \bar p,\quad e^\pm,\quad \mu^\pm.
$$

---

## 2. Main Components in LHCb

A simplified layout is:

```text
Interaction point
       |
       v
     VELO
       |
       v
      UT
       |
       v
    Magnet
       |
       v
     SciFi
       |
       v
   RICH / ECAL / HCAL
```

The main tracking-related components are:

- **VELO** — VErtex LOcator
- **UT** — Upstream Tracker
- **Magnet**
- **SciFi Tracker** — Scintillating Fibre Tracker

The Magnet is not itself a tracking detector. Its role is to bend charged-particle trajectories.

---

## 3. VELO

**VELO = VErtex LOcator.**

It is located very close to the proton-proton interaction region.

Its major role is precise reconstruction of:
- the primary vertex;
- secondary decay vertices;
- trajectories close to the collision point.

For example:

```text
Primary vertex
      ●
       \
        \
         ●  Secondary vertex
        / \
       /   \
      ●     ●
```

This is especially important for heavy-flavour physics, because particles containing heavy quarks can travel a measurable distance before decaying.

---

## 4. UT — Upstream Tracker

### Location

UT is located **upstream of the magnet**:

```text
VELO
  |
  v
 UT
  |
  v
Magnet
```

It measures particle hits before the particles enter the magnetic field.

### Detector technology

UT uses **silicon strip detectors**.

```text
| | | | | | | | | |
        ^
      particle
        |
| | | | | | | | | |
```

A charged particle deposits energy in the silicon and produces electrical charge. The readout identifies which strips were hit.

### Role

UT provides precise spatial measurements and information about the particle trajectory before the magnet. It also helps connect the upstream and downstream parts of a reconstructed track.

---

## 5. SciFi — Scintillating Fibre Tracker

### Location

SciFi is located **downstream of the magnet**:

```text
UT
 |
 v
Magnet
 |
 v
SciFi
```

It measures the particle after it has passed through the magnetic field and its trajectory has been bent.

### Detector technology

SciFi uses **scintillating fibres**.

When a charged particle passes through a scintillating fibre:

$$
\text{charged particle}
\rightarrow
\text{scintillation light}
\rightarrow
\text{photodetector}
\rightarrow
\text{electrical signal}
$$

The activated fibres provide the position information used to reconstruct hits.

### Role

SciFi provides downstream tracking information over a large detector area.

---

## 6. UT vs SciFi

The most important difference is their position relative to the magnet.

```text
             Magnet
               |
               v

UT                         SciFi
| | | |                  |||||||||
   \                         /
    \                       /
     \                     /
      \                   /
       \_________________/
```

| Feature | UT | SciFi |
|---|---|---|
| Full name | Upstream Tracker | Scintillating Fibre Tracker |
| Position | Before magnet | After magnet |
| Technology | Silicon strips | Scintillating fibres |
| Measures | Particle hits | Particle hits |
| Main role | Upstream trajectory information | Downstream trajectory information |
| Key advantage | Very precise spatial measurement | Large-area tracking coverage |

A useful mental model:

> **UT sees how the particle enters the magnet; SciFi sees how it leaves the magnet.**

Together, they provide information about how much the trajectory was bent.

---

## 7. Why is the Magnet Important?

A charged particle moving through a magnetic field experiences the Lorentz force:

$$
\vec F=q\vec v\times\vec B
$$

Therefore, its trajectory is bent.

In a simplified uniform magnetic field:

$$
p_T \approx 0.3\,|q|BR
$$

where:
- $p_T$ is the transverse momentum;
- $q$ is the particle charge;
- $B$ is the magnetic field;
- $R$ is the curvature radius.

Therefore:

$$
\boxed{
\text{trajectory curvature}
\rightarrow
\text{momentum}
}
$$

The bending direction also depends on the sign of the charge.

---

## 8. Why Do We Need Tracking on Both Sides of the Magnet?

```text
UT                    Magnet                  SciFi

●────●────●─────────> ╔═══════╗
                       ║       ║
                       ║       ║
                       ╚═══════╝
                              \
                               ●
                                \
                                 ●
                                  \
                                   ●
```

UT measures the incoming trajectory.

SciFi measures the outgoing trajectory.

Combining

$$
\text{upstream hits}
+
\text{downstream hits}
+
\text{magnetic field}
$$

allows the reconstruction software to determine the track curvature.

Then:

$$
\text{curvature}
\rightarrow
p
$$

and the bending direction gives the charge sign.

---




## 10. Silicon vs Scintillating Fibre Resolution

In general, **silicon strip detectors can provide better single-hit spatial resolution than scintillating-fibre detectors**.

Silicon strips can be made with fine pitch, and charge sharing between neighbouring strips can improve the position estimate.

Spatial resolution is typically at the scale of **tens of micrometres**, depending on detector design and reconstruction.

SciFi also provides good spatial resolution, while offering important advantages such as:
- large-area coverage;
- fast readout;
- suitability for the large downstream tracking region;
- a practical balance between performance, material, cost, and system complexity.

Thus detector design is not simply about maximizing spatial resolution. It balances:

$$
\boxed{
\text{spatial resolution}
+
\text{tracking efficiency}
+
\text{coverage}
+
\text{readout}
+
\text{material}
+
\text{cost}
}
$$

---

## 11. Tracking vs ECAL vs HCAL

| Detector | Main purpose | Main information |
|---|---|---|
| Tracking | Charged-particle tracking | Position, trajectory, momentum, charge |
| ECAL | Electromagnetic energy measurement | Energy of electromagnetic showers |
| HCAL | Hadronic energy measurement | Energy of hadronic showers |

For example, in

$$
B^0\rightarrow K^{*0}\gamma
$$

with

$$
K^{*0}\rightarrow K^+\pi^-,
$$

the tracking system reconstructs the $K^+$ and $\pi^-$ tracks and momenta, while the photon is mainly measured by the ECAL.

---

## 12. Important Tracking Performance Parameters

### Tracking efficiency

$$
\epsilon_{\rm tracking}
=
\frac{N_{\rm reconstructed}}
{N_{\rm true}}
$$

### Momentum resolution

$$
\frac{\sigma_p}{p}
$$

### Spatial resolution

$$
\sigma_x
$$

### Vertex resolution

The precision with which primary and secondary vertices are reconstructed.

This is especially important in heavy-flavour physics.

---

## 13. Big Picture

The whole tracking concept can be summarized as:

$$
\boxed{
\text{Charged particle}
\rightarrow
\text{detector hits}
\rightarrow
\text{track}
\rightarrow
\text{magnetic curvature}
\rightarrow
\text{momentum + charge}
}
$$

For LHCb, remember:

$$
\boxed{
\text{VELO + UT + Magnet + SciFi}
}
$$

- **VELO:** precise tracking and vertex reconstruction close to the interaction point.
- **UT:** silicon-strip tracking upstream of the magnet.
- **Magnet:** bends charged-particle trajectories.
- **SciFi:** scintillating-fibre tracking downstream of the magnet.
- **Combined tracking system:** reconstructs charged-particle tracks, momenta, and charge signs.

### One-sentence memory aid

> **UT measures how a charged particle enters the magnet, SciFi measures how it leaves, and the change in trajectory caused by the magnetic field tells us its momentum and charge.**

# LHCb RICH — Study Notes

## 1. What is RICH?

**RICH = Ring-Imaging Cherenkov detector**

RICH is mainly used for **Particle Identification (PID)**.

Its important role in LHCb is to distinguish charged hadrons such as:

$$
\pi,\quad K,\quad p
$$

The key idea is:

> **Tracking tells us how the particle moves and measures its momentum; RICH uses Cherenkov radiation to help determine what the particle is.**

---

## 2. Why Do We Need RICH?

The Tracking System can reconstruct a charged-particle track and measure its momentum and charge sign.

However, tracking alone does not directly tell us whether a charged particle is a pion, kaon, or proton.

For example, a positive track could be:

$$
\pi^+,\quad K^+,\quad p
$$

RICH provides additional particle-identification information.

---

## 3. Cherenkov Radiation

A charged particle moving through a medium can produce **Cherenkov radiation** when its speed exceeds the speed of light in that medium:

$$
v>\frac{c}{n}
$$

where:

- $c$ is the speed of light in vacuum;
- $n$ is the refractive index of the medium;
- $v$ is the particle velocity.

Using

$$
\beta=\frac{v}{c},
$$

the Cherenkov condition becomes:

$$
\boxed{\beta n>1}
$$

---

## 4. Cherenkov Cone

Cherenkov light is emitted at a characteristic angle rather than randomly in all directions.

The radiation forms a cone around the particle trajectory:

```text
             particle
                →
                →
                →

               \ | /
                \|/
                 V
                / \
               /   \
```

The characteristic angle is called the **Cherenkov angle**:

$$
\theta_C
$$

and satisfies:

$$
\boxed{
\cos\theta_C=\frac{1}{n\beta}
}
$$

This is the central equation of RICH physics.

---

## 5. Why Can RICH Distinguish Different Particles?

At a fixed momentum, different particle species have different masses.

Relativistically:

$$
E^2=p^2c^2+m^2c^4
$$

and

$$
\beta=\frac{v}{c}
=\frac{pc}{E}
$$

Therefore:

$$
\boxed{
\beta=
\frac{pc}
{\sqrt{p^2c^2+m^2c^4}}
}
$$

For the same momentum, heavier particles generally have smaller $\beta$.

Since

$$
\cos\theta_C=\frac{1}{n\beta},
$$

different particle species produce different Cherenkov angles.

For example, at the same momentum, approximately:

$$
m_\pi<m_K<m_p
$$

so:

$$
\beta_\pi>\beta_K>\beta_p
$$

and therefore:

$$
\boxed{
\theta_C(\pi)>\theta_C(K)>\theta_C(p)
}
$$

provided all three particles are above the Cherenkov threshold.

---

## 6. From Cherenkov Cone to Ring

The detector is called **Ring-Imaging** because the Cherenkov cone is converted into a ring-like image.

Conceptually:

```text
Particle
   |
   v
Cherenkov cone
   |
   v
Optical system
   |
   v
Photon detector

        ********
      **        **
     *            *
     *     ●      *
      **        **
        ********
```

The radius of the reconstructed ring is related to the Cherenkov angle.

Therefore:

$$
\boxed{
\text{ring image}
\rightarrow
\theta_C
}
$$

---

## 7. What Does RICH Actually Measure?

RICH does not primarily measure momentum.

It primarily measures:

$$
\boxed{\theta_C}
$$

The momentum comes mainly from the Tracking System.

The two systems work together:

```text
Tracking
   |
   | → momentum p
   |
   v
 RICH
   |
   | → Cherenkov angle θC
   |
   v
Particle Identification
```

Thus the basic PID information is:

$$
\boxed{
p+\theta_C
\rightarrow
\text{particle identity}
}
$$

---

## 8. PID Hypotheses

Suppose Tracking measures:

$$
p=10\ \mathrm{GeV}/c
$$

and RICH measures a Cherenkov angle:

$$
\theta_C^{\rm measured}
$$

We can test different particle hypotheses:

$$
H_\pi,\quad H_K,\quad H_p
$$

For each hypothesis, the expected Cherenkov angle can be calculated:

$$
\theta_C^\pi,\quad
\theta_C^K,\quad
\theta_C^p
$$

Then the measured angle can be compared with the predictions.

Conceptually:

```text
Measured θC
     |
     +---- compare with π hypothesis
     |
     +---- compare with K hypothesis
     |
     +---- compare with p hypothesis
     |
     v
PID information
```

The reconstruction software uses the agreement between the observed Cherenkov information and each particle hypothesis to obtain PID information.

---

## 9. RICH Radiator

RICH needs a transparent medium in which Cherenkov radiation can be produced.

This material is called the **radiator**.

The basic process is:

$$
\text{charged particle}
\rightarrow
\text{radiator}
\rightarrow
\text{Cherenkov photons}
$$

Different radiator materials can be used to cover different particle momentum ranges because their refractive indices are different.

---

## 10. RICH Signal Chain

The complete process can be summarized as:

```text
Charged particle
       ↓
    Radiator
       ↓
Cherenkov radiation
       ↓
Cherenkov cone
       ↓
Optical system
       ↓
Ring image
       ↓
Photon detector
       ↓
Photon hits
       ↓
Ring reconstruction
       ↓
Cherenkov angle θC
       ↓
Combine with momentum
       ↓
Particle identification
```

This follows the same general detector-physics logic used for ECAL, HCAL, and Tracking:

$$
\boxed{
\text{particle}
\rightarrow
\text{physical interaction}
\rightarrow
\text{detector signal}
\rightarrow
\text{reconstruction}
\rightarrow
\text{physics information}
}
$$

---

## 11. RICH vs Tracking

| Feature | Tracking | RICH |
|---|---|---|
| Main purpose | Track reconstruction | Particle identification |
| Main measurement | Position / trajectory | Cherenkov angle |
| Important output | Momentum and charge | PID information |
| Core physics | Magnetic bending | Cherenkov radiation |
| Typical use | Reconstruct charged-particle kinematics | Distinguish $\pi$, $K$, $p$ |

A useful memory aid:

> **Tracking tells us how the particle moves; RICH tells us what the particle may be.**

---

## 12. Example: $B^0\rightarrow K^{*0}\gamma$

Consider:

$$
B^0\rightarrow K^{*0}\gamma
$$

with

$$
K^{*0}\rightarrow K^+\pi^-.
$$

Tracking reconstructs the charged-particle tracks and their momenta:

$$
p_{K^+},\qquad p_{\pi^-}
$$

However, identifying which track is a kaon and which is a pion requires particle-identification information.

RICH provides information for:

$$
\boxed{K/\pi\ \text{separation}}
$$

while the photon is mainly measured by the ECAL.

Thus:

```text
K+ / π−
   |
   v
Tracking → momentum + charge
   |
   v
RICH → PID

γ
|
v
ECAL → electromagnetic energy
```

---

## 13. Core Physics Chain

The whole RICH concept can be reduced to five steps.

### Step 1 — Tracking measures momentum

$$
\boxed{p}
$$

### Step 2 — Particle enters the radiator

$$
\boxed{\text{charged particle}}
$$

### Step 3 — Cherenkov radiation is produced

Condition:

$$
\boxed{\beta n>1}
$$

### Step 4 — RICH measures the Cherenkov angle

$$
\boxed{
\cos\theta_C=\frac{1}{n\beta}
}
$$

### Step 5 — Combine momentum and Cherenkov angle

$$
\boxed{
p+\theta_C
\rightarrow
\pi,\ K,\ p
}
$$

---


### PID principle

$$
\boxed{
\text{momentum}
+
\text{Cherenkov angle}
\rightarrow
\text{particle identification}
}
$$

---

# 15. Big Picture: Tracking + RICH

The relationship between the two systems is:

```text
                 Charged particle
                        |
                        v
                   Tracking
                        |
             ┌──────────┴──────────┐
             ↓                     ↓
        trajectory             momentum p
             |                     |
             └──────────┬──────────┘
                        ↓
                       RICH
                        |
                        ↓
                 Cherenkov angle
                     θC
                        |
                        ↓
                  Particle ID
                  π / K / p
```

The key idea is:

> **Tracking provides the momentum; RICH provides the Cherenkov angle; together they allow particle identification.**

---

# 16. One-Sentence Memory Aid

> **RICH uses Cherenkov radiation to measure the Cherenkov angle; combined with the momentum measured by the tracking system, this provides particle-identification information for charged particles such as pions, kaons, and protons.**


## ECAL
## 1. 基本概念

**ECAL** = **Electromagnetic Calorimeter**

中文通常称为：

* 电磁量能器

在 CERN 的 **LHCb（Large Hadron Collider beauty）实验**中，ECAL 是重要的量能器子探测器之一。

它主要用于测量：

* 光子（\(\gamma\)）的能量和位置
* 电子（\(e^-\)）/正电子（\(e^+\)）的能量
* 电磁簇射（electromagnetic shower）

---

# 2. ECAL 在 LHCb 中的位置和作用

LHCb 是 LHC 上专门研究重味物理的前向谱仪，重点研究：

* \(b\) 夸克和 \(c\) 夸克相关粒子
* CP violation（CP 破坏）
* 稀有衰变（rare decays）
* 标准模型精密检验
* 新物理效应

ECAL 是 LHCb 粒子鉴别和能量测量系统的一部分。

对于从碰撞点向前飞行的粒子，可以粗略理解为依次经过：

```text
pp collision
     ↓
Tracking detectors
     ↓
RICH detectors
     ↓
ECAL
     ↓
HCAL
     ↓
Muon system
```

不同探测器承担不同任务：

| 子探测器        | 主要功能                |
| ----------- | ------------------- |
| Tracking    | 测量带电粒子的轨迹和动量        |
| RICH        | 粒子鉴别，例如 \(\pi/K/p\) |
| ECAL        | 测量电子、光子的电磁能量        |
| HCAL        | 测量强子能量              |
| Muon system | μ 子识别               |

---

# 3. ECAL 的核心工作原理

ECAL 的基本任务可以概括为：

$$
\boxed{
\text{粒子能量}
\rightarrow
\text{电磁簇射}
\rightarrow
\text{闪烁光}
\rightarrow
\text{电信号}
}
$$

最终通过测量电信号大小，反推出入射粒子的能量。

---

# 4. 电磁簇射

以高能光子为例。

光子进入 ECAL 后，可以发生：

$$
\gamma \rightarrow e^+ + e^-
$$
不能在真空中单独发生，需要原子核反冲。
产生的电子和正电子继续发生辐射：

$$
e^\pm \rightarrow e^\pm + \gamma
$$
这是轫致辐射，电子经过原子核附近时，被原子核的电磁场“偏转/减速”，于是辐射出光子。
产生的新光子又可以继续产生电子-正电子对。

因此形成级联过程：

$$
\gamma
\rightarrow e^+e^-
\rightarrow e^\pm+\gamma
\rightarrow e^+e^-+\cdots
$$

最终形成大量电子、正电子和光子的集合，即：

**Electromagnetic Shower（电磁簇射）**

---

# 5. LHCb ECAL 的结构

LHCb ECAL 使用类似 **Shashlik calorimeter** 的结构。

其基本结构可以理解为：

```text
        入射粒子
            ↓
    ┌──────────────┐
    │     Lead     │  ← 促进电磁簇射
    ├──────────────┤
    │  Scintillator │  ← 能量 → 闪烁光
    ├──────────────┤
    │     Lead     │
    ├──────────────┤
    │  Scintillator │
    ├──────────────┤
    │      ...     │
    └──────────────┘
          ↓
        光纤
          ↓
    光探测器
          ↓
       电信号
```

核心材料/部件包括：

1. **铅（Lead）**
2. **闪烁体（Scintillator）**
3. **光纤（Optical fibers）**
4. **光探测器**

---

# 6. 铅的作用

铅主要用于促进高能电子和光子的电磁簇射。

它具有较高的密度和较短的辐射长度，因此可以让电磁簇射在相对有限的空间内发展。

可以简单理解为：

> 铅负责让入射电子/光子产生大量次级粒子。

---

# 7. 闪烁体的作用

带电粒子穿过闪烁体时，会激发闪烁材料。

随后材料从激发态返回较低能级，并产生可见光：

$$
\text{Excited state}
\rightarrow
\text{Ground state}
+
\gamma_{\text{visible}}
$$

因此实现：

$$
\boxed{
\text{沉积能量}
\rightarrow
\text{闪烁光}
}
$$

入射粒子能量越高，通常产生的闪烁光越多。

---

# 8. 光纤的作用

闪烁体产生的光需要被传输到光探测器。

光纤负责：

$$
\boxed{
\text{收集并传输闪烁光}
}
$$

最终将光信号送到光探测器。

---

# 9. 光探测器和电子学

光进入光探测器后，被转换为电信号。

整个信号链可以简化为：

```text
Incident particle
       ↓
Electromagnetic shower
       ↓
Energy deposition
       ↓
Scintillation light
       ↓
Optical fiber
       ↓
Photodetector
       ↓
Electronic signal
       ↓
ADC / readout
       ↓
Reconstructed energy
```

因此最终：

$$
E_{\text{particle}}
\propto
N_{\text{photons}}
\propto
Q_{\text{signal}}
$$

经过探测器标定（calibration）后，可以由信号大小得到粒子能量。

---

# 10. ECAL 如何测量粒子位置？

ECAL 不是一个单一的大块探测材料，而是由大量独立的 **cells（探测单元）**组成。

例如：

```text
┌───┬───┬───┬───┬───┐
│   │   │   │   │   │
├───┼───┼───┼───┼───┤
│   │   │ █ │   │   │
├───┼───┼───┼───┼───┤
│   │   │ █ │   │   │
└───┴───┴───┴───┴───┘
```

电磁簇射通常会覆盖多个相邻 cell。

通过分析不同 cell 中的能量沉积，可以重建：

* 总能量
* 横向位置
* 电磁簇射形状

---

# 11. ECAL 和 RICH 的区别

这两个系统在 LHCb 中承担不同任务。

### RICH

主要回答：

> “这个带电粒子是什么？”

例如：

$$
\pi,\ K,\ p
$$

RICH 主要用于粒子鉴别（Particle Identification, PID）。

### ECAL

主要回答：

> “这个电子/光子有多少能量？在哪里？”

所以：

$$
\boxed{
\text{RICH} \rightarrow \text{Particle ID}
}
$$

$$
\boxed{
\text{ECAL} \rightarrow \text{Electromagnetic Energy Measurement}
}
$$

两者可以互相配合。

---

# 12. 一个典型例子：\(B^0\rightarrow K^{*0}\gamma\)

考虑衰变：

$$
B^0\rightarrow K^{*0}\gamma
$$

其中存在一个光子：

$$
\gamma
$$

光子不会像带电粒子一样在磁场中产生可测量的弯曲轨迹。

因此 ECAL 对光子的测量非常重要。

一个典型的信息组合可以是：

```text
Tracking
    ↓
带电粒子的轨迹 / 动量

RICH
    ↓
K / π 等粒子鉴别

ECAL
    ↓
γ 的能量和位置

HCAL
    ↓
强子能量

Muon system
    ↓
μ 子识别
```

最终将这些信息组合起来，重建整个衰变过程。

---

# 13. 另一个例子：\(\pi^0\rightarrow\gamma\gamma\)

中性 pion 可以衰变：

$$
\pi^0\rightarrow\gamma\gamma
$$

ECAL 可以测量两个光子：

$$
\gamma_1,\gamma_2
$$

然后利用它们的：

* 能量
* 方向

重建 \(\pi^0\)。

两个光子的不变质量满足：

$$
m_{\gamma\gamma}^2
=
2E_1E_2(1-\cos\theta)
$$

其中：

* \(E_1\)：第一个光子的能量
* \(E_2\)：第二个光子的能量
* \(\theta\)：两个光子的夹角

因此 ECAL 的能量和位置分辨率会直接影响最终的质量重建精度。

---

# 14. 什么是 Energy Resolution？

ECAL 不可能每次都完美测出真实能量。

假设真实能量：

$$
E=10\text{ GeV}
$$

多次测量可能得到：

$$
9.7,\ 10.2,\ 9.9,\ 10.1,\ 9.8\text{ GeV}
$$

这些测量值会围绕平均值波动。

用标准差：

$$
\sigma_E
$$

描述这种波动。

通常定义相对能量分辨率：

$$
\boxed{
\frac{\sigma_E}{E}
}
$$

这个数越小，表示能量测量越精确。

---

# 15. ECAL 的 Energy Resolution 参数化

常见的量能器能量分辨率表达式为：

$$
\boxed{
\frac{\sigma_E}{E}
=
\frac{a}{\sqrt E}
\oplus
b
\oplus
\frac{c}{E}
}
$$

其中：

$$
A\oplus B
=
\sqrt{A^2+B^2}
$$

因此完整形式为：

$$
\boxed{
\frac{\sigma_E}{E}
=
\sqrt{
\frac{a^2}{E}
+
b^2
+
\frac{c^2}{E^2}
}
}
$$

通常 \(E\) 使用 GeV。

---

# 16. 三个分辨率项

## 16.1 Stochastic term

$$
\boxed{
\frac{a}{\sqrt E}
}
$$

称为 **stochastic term（随机项）**。

主要与：

* 光子统计
* 电磁簇射涨落
* 能量沉积统计涨落

等有关。

由于：

$$
N_{\text{photons}}\propto E
$$

而统计涨落近似：

$$
\sigma_N\sim\sqrt N
$$

因此：

$$
\frac{\sigma_N}{N}
\sim
\frac{1}{\sqrt N}
\sim
\frac{1}{\sqrt E}
$$

所以产生：

$$
\frac{a}{\sqrt E}
$$

这一项。

---

## 16.2 Constant term

$$
\boxed{b}
$$

称为 **constant term（常数项）**。

可能来源包括：

* cell 响应不一致
* 校准误差
* 探测器非均匀性
* 能量泄漏
* 温度变化
* 长期稳定性
* 电子学系统等

当：

$$
E\rightarrow\infty
$$

时：

$$
\frac{a}{\sqrt E}\rightarrow0
$$

因此高能区域最终可能由：

$$
\boxed{b}
$$

限制能量分辨率。

---

## 16.3 Noise term

$$
\boxed{
\frac{c}{E}
}
$$

称为 **noise term（噪声项）**。

可能来源包括：

* Electronic noise
* Pedestal fluctuations
* 背景
* Pile-up 等

它在低能量区域更加重要。

如果噪声大小近似固定：

$$
\sigma_{\text{noise}}\approx\text{constant}
$$

那么相对于粒子能量的影响就是：

$$
\frac{\sigma_{\text{noise}}}{E}
\propto
\frac1E
$$

因此得到：

$$
\frac{c}{E}
$$

---

# 17. 三项的直观理解

| 能量区域 | 主要影响                        | 形式            |
| ---- | --------------------------- | ------------- |
| 低能   | Noise                       | \(c/E\)       |
| 中等能量 | Statistical fluctuations    | \(a/\sqrt E\) |
| 高能   | Detector/systematic effects | \(b\)         |

可以简单记成：

```text
低能                    高能
 │                        │
 │ Noise                  │ Constant
 │ ↓                      │ ↓
 ├────────────────────────┤
 │      Stochastic        │
 │      1 / √E            │
 └────────────────────────┘
```

重要直觉：

> **能量越高，通常相对能量分辨率越好，但不会无限变好。**

因为在高能区最终会受到 constant term 的限制。

---


# 19. ECAL 为什么对 LHCb 物理分析重要？

ECAL 的测量会影响很多后续的物理量。

例如：

$$
\pi^0\rightarrow\gamma\gamma
$$

需要利用：

$$
E_1,\ E_2,\ \theta
$$

计算：

$$
m_{\gamma\gamma}^2
=
2E_1E_2(1-\cos\theta)
$$

因此：

$$
\boxed{
\text{ECAL Energy Resolution}
\rightarrow
\text{Energy Measurement}
\rightarrow
\text{Invariant Mass Resolution}
}
$$

也就是说，ECAL 的性能最终会影响粒子重建和物理分析的精度。

---

# 20. 最重要的知识框架

可以把 LHCb ECAL 总结为下面这条链：

```text
                 LHCb ECAL
                     │
                     ↓
          Electromagnetic particles
              γ / e⁺ / e⁻
                     │
                     ↓
          Electromagnetic shower
                     │
                     ↓
             Energy deposition
                     │
                     ↓
              Scintillation
                     │
                     ↓
              Optical fibers
                     │
                     ↓
             Photodetector
                     │
                     ↓
              Electronic signal
                     │
                     ↓
                 Readout
                     │
                     ↓
            Energy reconstruction
                     │
                     ↓
        Physics quantities / analysis
```

---

---

# 22. 一句话总结

> **LHCb 的 ECAL 是一个用于测量电子和光子能量、位置及电磁簇射特征的电磁量能器。它通过铅产生电磁簇射、闪烁体将能量转换为光、光纤传输光信号、光探测器将其转换成电信号，最终经过电子学读出和校准重建粒子的能量。其性能通常用 \(\sigma_E/E\) 描述，并可用 \(a/\sqrt E\oplus b\oplus c/E\) 参数化。**






# LHCb HCAL --- Study Notes

## 1. What is HCAL?

**HCAL** stands for **Hadron Calorimeter**.

In the LHCb experiment at CERN, HCAL is the calorimeter system primarily
designed to measure the energy deposited by **hadrons**, such as:

-   Protons: (p)
-   Neutrons: (n)
-   Charged and neutral pions
-   Kaons
-   Other hadrons produced in high-energy collisions

HCAL is located downstream of the **ECAL (Electromagnetic
Calorimeter)**.

------------------------------------------------------------------------

## 2. Why Does LHCb Need HCAL?

Different particles interact with detector material through different
physical processes.

### Electromagnetic particles

Electrons, positrons, and photons mainly produce **electromagnetic
showers** .These are primarily measured by **ECAL**.

### Hadrons

Hadrons interact strongly with the detector material and produce
**hadronic showers**.

Therefore:

\[ \boxed{
\text{ECAL} \rightarrow \text{electromagnetic shower}
} \]

\[ \boxed{
\text{HCAL} \rightarrow \text{hadronic shower}
} \]

This is the main conceptual distinction between the two calorimeters.

------------------------------------------------------------------------


# 4. Hadronic Showers

Consider a high-energy proton entering HCAL.

It can undergo strong interactions with nuclei in the detector material:

\[ p + \text{nucleus} \rightarrow
\text{many secondary particles} \]

The secondary particles can include:

\[ \pi, K, p, n,\ldots \]

These particles interact again, producing further generations of
particles.

The result is a **hadronic shower**:

``` text
                 Hadron
                    ↓
                    ↓
              ┌───────────┐
              │   Iron    │
              └───────────┘
                ↙  ↓  ↘
              π    p    n
             ↙ ↓  ↓  ↘
          more secondary particles
                  ↓
              shower
```

Unlike an electromagnetic shower, a hadronic shower is driven mainly by
**strong interactions** and is generally more complicated.

------------------------------------------------------------------------

# 5. LHCb HCAL Structure

The LHCb HCAL is a **sampling calorimeter**.

Its basic structure consists of alternating layers of:

-   **Iron absorber**
-   **Scintillating tiles**

A simplified picture is:

``` text
Incoming hadron
       ↓
┌─────────────────┐
│      Iron       │  ← absorber
├─────────────────┤
│  Scintillator   │  ← active layer
├─────────────────┤
│      Iron       │
├─────────────────┤
│  Scintillator   │
├─────────────────┤
│      Iron       │
├─────────────────┤
│  Scintillator   │
├─────────────────┤
│       ...       │
└─────────────────┘
       ↓
 Optical fibers
       ↓
      PMT
       ↓
 Electrical signal
```

The basic principle is:

\[ \boxed{
\text{Absorber} + \text{Active material}
} \]

------------------------------------------------------------------------

# 6. Role of the Iron

The iron acts mainly as the **absorber** and provides material in which
the hadronic shower develops.

When a high-energy hadron enters the iron, it undergoes strong
interactions and produces secondary particles.

Thus, in simplified terms:

\[ \boxed{
\text{Iron}
\rightarrow
\text{Hadronic interactions}
\rightarrow
\text{Hadronic shower}
} \]

The shower then passes through successive layers of the calorimeter.

------------------------------------------------------------------------

# 7. Role of the Scintillator

The scintillating tiles are the **active detector material**.

Charged particles from the shower pass through the scintillator and
deposit energy.

This energy excites the scintillator material, which subsequently emits
light:

\[ \text{Excited state}\rightarrow
\text{Lower-energy state} + \text{scintillation photon}
\]

Therefore:

\[ \boxed{
\text{Deposited energy}
\rightarrow
\text{Scintillation light}
} \]

The amount of light is related to the amount of energy deposited in the
active material.

------------------------------------------------------------------------

# 8. Optical Fibers and PMTs

The scintillation light is collected and transported by
**wavelength-shifting (WLS) fibers**.

The fibers guide the light to **photomultiplier tubes (PMTs)**.

The signal chain can therefore be summarized as:

\[ 
\text{Hadron}
\rightarrow
\text{Hadronic shower}
\rightarrow
\text{Energy deposition}
\rightarrow
\text{Scintillation light}
\rightarrow

\]
\[
\text{WLS fiber}
\rightarrow
\text{PMT}
\rightarrow
\text{Electrical signal}\]

The electrical signal is then digitized and processed to reconstruct
detector observables.

------------------------------------------------------------------------


------------------------------------------------------------------------

# 10. Energy Deposition in Both ECAL and HCAL

Suppose a hadron enters LHCb. It may deposit part of its energy in ECAL and the remaining part in HCAL:

``` text
Incoming hadron
       ↓
┌──────────────┐
│     ECAL     │
│  part of E   │
└──────────────┘
       ↓
┌──────────────┐
│     HCAL     │
│  more of E   │
└──────────────┘
```

In a simple approximation:

\[ E\_\text{hadron}\approx E\_{\text{ECAL}} +
E\_{\text{HCAL}} \]

However, the real reconstruction is more complicated.

The raw detector signals cannot simply be added together because ECAL and HCAL have different responses and because hadronic showers fluctuate.

------------------------------------------------------------------------

# 11. Why Is Hadron Energy Measurement Difficult?

Hadronic energy measurement is more complicated than electromagnetic
energy measurement for several reasons.

## 11.1 Hadronic shower fluctuations

Different hadrons with the same initial energy can produce different
shower compositions.

For example, part of the shower energy may be converted into neutral
pions:

\[ \pi^0\rightarrow\gamma\gamma \]

The resulting photons generate electromagnetic shower components.

Other parts remain in hadronic form.

Thus a hadronic shower can contain both:

\[ \boxed{
\text{Electromagnetic component}
+
\text{Hadronic component}
}\]

------------------------------------------------------------------------

## 11.2 Non-compensation

A hadronic calorimeter generally does not respond identically to
electromagnetic and hadronic energy.

This is often expressed using:
\[ \boxed{
e/h}\]

where (e) represents the response to electromagnetic energy and (h)
represents the response to hadronic energy.

For an ideal compensating calorimeter:

\[ e/h=1 \]

In many practical sampling calorimeters:

\[ e/h\neq1\]

Therefore, two showers with the same initial energy can produce
different detector responses depending on their electromagnetic
fraction.

------------------------------------------------------------------------

## 11.3 Invisible energy

Not all of the initial hadron energy becomes detectable scintillation
light.

Some energy can go into processes such as:

-   Nuclear excitation
-   Nuclear breakup
-   Binding-energy losses
-   Low-energy particles with limited detector response

This is often referred to as **invisible energy**.

A simplified energy balance is:

\[ `\boxed{
E_{\text{initial}}
=
E_{\text{visible}}
+
E_{\text{invisible}}
+
E_{\text{leakage}}
}\]

------------------------------------------------------------------------

## 11.4 Leakage

If the shower is not fully contained within the calorimeter, some energy
can escape.

This is called **shower leakage**.

Therefore:

\[ E\_{\text{measured}} < E\_{\text{initial}} \]

can occur even when the detector electronics are working perfectly.

------------------------------------------------------------------------

# 12. Calibration and Energy Reconstruction

Because the raw ECAL and HCAL signals are not direct measurements of the
original hadron energy, calibration is required.

A simplified reconstruction can be represented as:

\[ \boxed{
E_{\text{reco}}
=
\alpha E_{\text{ECAL}}
+
\beta E_{\text{HCAL}}
}\]

where ($\alpha$) and ($\beta$) represent calibration factors.

Real reconstruction can be more sophisticated and may use information
such as:

-   ECAL and HCAL cluster energies
-   Cluster positions
-   Shower shapes
-   Detector response
-   Leakage corrections
-   Background and pile-up conditions
-   Particle type
-   Other detector information

The calibration constants are determined from dedicated calibration data
and physics samples.

------------------------------------------------------------------------

# 13. Charged Hadrons: Tracking Also Helps

A particularly important feature of LHCb is that **charged hadrons leave
tracks**.

For example:

\[ \pi^\pm, K^\pm, p \]

are deflected by the magnetic field, allowing the tracking system to
measure their momentum:

\[ p \]

If the particle mass is known or identified, its energy can be obtained
from:

\[ \boxed{
E=\sqrt{p^2c^2+m^2c^4}
}\]

Therefore, for charged hadrons, LHCb does not rely exclusively on HCAL
for energy information.

Instead, tracking and calorimeter information can be complementary.

------------------------------------------------------------------------

# 14. Neutral Hadrons

Neutral hadrons such as neutrons do not produce the same type of
charged-particle track in the tracking system.

For such particles, calorimeter measurements are much more important for
determining their energy.

This illustrates why HCAL is particularly important for neutral hadronic
energy measurements.

------------------------------------------------------------------------

# 15. Interaction Length

For electromagnetic calorimeters, a key length scale is the **radiation
length**:

\[ X_0 \]

For hadronic calorimeters, an important scale is the **nuclear
interaction length**:

\[ \boxed{\lambda_I} \]

The interaction length characterizes the typical scale over which a
high-energy hadron undergoes a nuclear interaction in a material.

A useful conceptual distinction is:

\[ \boxed{
X_0
\rightarrow
\text{Electromagnetic shower}
} \]

\[ \boxed{
\lambda_I
\rightarrow
\text{Hadronic shower}
}\]

The LHCb HCAL has a depth of approximately:

\[ \boxed{5.6\lambda_I} \]

This depth helps contain the hadronic shower.

------------------------------------------------------------------------

# 17. ECAL and HCAL Are Complementary

It is incorrect to think of ECAL and HCAL as two completely independent
detectors that measure completely different energy samples.

A more accurate picture is:

``` text
                   Hadron
                     ↓
              ┌────────────┐
              │    ECAL    │
              │  EM + some │
              │   hadronic │
              │ deposition │
              └────────────┘
                     ↓
              ┌────────────┐
              │    HCAL    │
              │  hadronic  │
              │ deposition │
              └────────────┘
                     ↓
```

The full shower can extend across both systems.

Therefore, the reconstruction must combine the information
appropriately.

------------------------------------------------------------------------

# 18. Overall HCAL Signal Chain

The complete picture can be summarized as:

``` text
High-energy hadron
        ↓
Hadronic interactions
        ↓
Hadronic shower
        ↓
Energy deposition
        ↓
Scintillation in active layers
        ↓
Wavelength-shifting fibers
        ↓
Photomultiplier tubes
        ↓
Electrical signal
        ↓
Digitization / readout
        ↓
Calibration
        ↓
Energy reconstruction
        ↓
Physics analysis
```

------------------------------------------------------------------------


------------------------------------------------------------------------

# 20. One-Sentence Summary

> **The LHCb HCAL is a sampling hadron calorimeter that uses iron
> absorber layers and scintillating tiles to develop and sample hadronic
> showers, converting deposited energy into scintillation light and then
> electrical signals; because hadronic showers can extend across both
> ECAL and HCAL and contain electromagnetic, hadronic, invisible, and
> escaping components, accurate hadron-energy reconstruction requires
> calibration and the combination of information from multiple detector
> systems.**



# LHCb Muon System 


## 1. Overview

The **Muon System** is one of the key sub-detectors of the LHCb experiment.

Its primary purpose is:

> **To identify muons ($\mu^\pm$) and provide spatial and timing information associated with muon candidates.**

The Muon System is located at the downstream end of LHCb, after the tracking detectors and calorimeters.



The basic idea is that most particles are absorbed or significantly degraded before reaching the Muon System, while high-energy muons have a high probability of penetrating through the detector material.

---

# 2. Why Can Muons Reach the Muon System?

A very important clarification is:

> **It is not true that only muons can reach the Muon System.**

Hadrons can occasionally penetrate the calorimeter, a phenomenon known as **punch-through**. Electrons can also produce signals in downstream material.

However, muons are much more likely to traverse the calorimeters and reach the Muon System while retaining a clear penetrating-particle signature.

The main reason is the different ways particles interact with matter.

---

# 3. Muons vs. Other Particles

## 3.1 Muons

A muon is a lepton:

$$
\mu^\pm
$$

It does **not participate in the strong interaction**.

Its main energy-loss mechanism in the relevant energy range is approximately:

$$
\text{ionization and excitation}
$$

Thus, a muon tends to lose energy gradually:

```text
Muon
  │
  ▼
 ─────────────── Material
      ↓ small energy loss
 ─────────────── Material
      ↓ small energy loss
 ─────────────── Material
      ↓ small energy loss
 ─────────────── Material
  │
  ▼
Muon System
```

It therefore has a high penetration capability.

---

## 3.2 Hadrons

Examples include:

$$
\pi^\pm,\quad K^\pm,\quad p,\quad \bar p
$$

Hadrons participate in the strong interaction.

When a high-energy hadron enters the calorimeter, it can interact with nuclei and produce a **hadronic shower**:

```text
π
│
▼
Interaction
├── π
├── K
├── π
├── ...
│
▼
More interactions
│
▼
Hadronic shower
```

The original particle's energy is distributed among many secondary particles and deposited in the calorimeter.

Therefore, most hadrons do not reach the Muon System as intact high-energy particles.

Some hadrons can nevertheless penetrate the calorimeter and create background hits. This is called:

$$
\boxed{\text{hadron punch-through}}
$$

---

## 3.3 Electrons

Electrons are also leptons and do not participate in the strong interaction.

However, electrons are much lighter than muons:

$$
m_e \approx 0.511\ \mathrm{MeV}
$$

while

$$
m_\mu \approx 105.7\ \mathrm{MeV}
$$

Therefore,

$$
m_\mu \approx 207m_e
$$

Electrons are much more susceptible to **Bremsstrahlung** in matter:

$$
e^- \rightarrow e^-+\gamma
$$

The emitted photons can subsequently produce electron-positron pairs:

$$
\gamma\rightarrow e^+e^-
$$

leading to an **electromagnetic shower**.

Thus electrons typically deposit most of their energy in the ECAL rather than behaving like penetrating muons.

---

# 4. Key Physical Reason for Muon Penetration

The main reasons for the strong penetrating ability of muons are:

### 1. No strong interaction

$$
\mu + N
\not\rightarrow
\text{hadronic shower}
$$

Unlike hadrons, muons do not undergo strong nuclear interactions.

### 2. Relatively small energy loss

In the relevant energy range, muons primarily lose energy through ionization:

$$
-\frac{dE}{dx}
$$

Their energy is gradually reduced rather than rapidly converted into a large shower.

### 3. Large mass compared with electrons

Because

$$
m_\mu \gg m_e
$$

muons undergo much less Bremsstrahlung than electrons at comparable energies.

Therefore:

$$
\boxed{
\text{No strong interaction}
+
\text{moderate ionization loss}
+
\text{large mass}
\Rightarrow
\text{high penetration capability}
}
$$

---

# 5. Calorimeters as a Particle Filter

The calorimeter system plays an important role in separating particle types.

## Electromagnetic particles

Electrons and photons produce electromagnetic showers:

$$
e^\pm,\gamma
\rightarrow
\text{electromagnetic shower}
$$

These are primarily measured in the **ECAL**.

## Hadrons

Pions, kaons, protons, etc. produce hadronic showers:

$$
\pi/K/p
\rightarrow
\text{hadronic shower}
$$

These are primarily measured in the **HCAL**.

## Muons

Muons tend to pass through both calorimeters with comparatively moderate energy loss:

$$
\mu
\rightarrow
\text{penetrates ECAL + HCAL}
\rightarrow
\text{Muon System}
$$

This is the physical basis of the Muon System.

---


# 7. Detector Technologies

The LHCb Muon System mainly uses **gas-based detectors**.

Important technologies include:

### MWPC

**Multi-Wire Proportional Chamber**

A charged particle passing through the gas ionizes the gas. The resulting electrons are amplified in the electric field near the wires, producing a measurable signal.



### GEM

**Gas Electron Multiplier**

GEM technology uses microscopic holes in thin foils to produce electron avalanches and provide fast amplification.

GEM technology is particularly useful in regions where high particle rates require good rate capability.

---

# 8. Why Are Multiple Muon Stations Needed?

A single hit is not sufficient to establish that a particle is a muon.

Instead, multiple stations provide a **hit pattern**:

```text
Muon
 │
 ├───────────────● M2
 │
 ├──────────────────● M3
 │
 ├─────────────────────● M4
 │
 └────────────────────────● M5
```

The experiment can determine whether the hits are consistent with a particle trajectory.

Muon identification can combine:

* Muon-station hits
* Tracking information
* Momentum
* Calorimeter information
* RICH particle-identification information

Thus, muon identification is not simply:

> "A hit in the Muon System means muon."

Instead, it is a combined particle-identification problem.

---

# 9. Relationship with the LHCb Magnet

The LHCb dipole magnet bends charged-particle trajectories.

For a charged particle moving in a magnetic field, the curvature is related to its momentum:

$$
p_T \propto qBR
$$

where:

* $p_T$ is the transverse momentum
* $q$ is the particle charge
* $B$ is the magnetic field
* $R$ is the curvature radius

Tracking detectors measure the trajectory before and after the magnet.

The Muon System then provides downstream information that can be matched to the reconstructed track.

Therefore:

$$
\boxed{
\text{Tracking}
+
\text{Magnet}
+
\text{Muon System}
}
$$

provides much more information than the Muon System alone.

---

# 10. Role in Particle Identification

A simplified particle-identification picture is:

```text
                 Particle
                    │
                    ▼
              ┌───────────┐
              │  Tracking │
              └───────────┘
                    │
                    ▼
              ┌───────────┐
              │   RICH    │
              │  π/K/p ID │
              └───────────┘
                    │
                    ▼
              ┌───────────┐
              │   ECAL    │
              │  e / γ    │
              └───────────┘
                    │
                    ▼
              ┌───────────┐
              │   HCAL    │
              │  hadrons  │
              └───────────┘
                    │
                    ▼
              ┌───────────┐
              │   MUON    │
              │    μ ID   │
              └───────────┘
```

The detectors therefore provide complementary information:

| Detector    | Main role                                          |
| ----------- | -------------------------------------------------- |
| VELO        | Precise vertexing and tracking                     |
| UT          | Upstream tracking                                  |
| Magnet      | Momentum measurement through track curvature       |
| SciFi       | Downstream tracking                                |
| RICH        | Hadron/lepton PID, especially $\pi/K/p$ separation |
| ECAL        | Electromagnetic energy measurement                 |
| HCAL        | Hadronic energy measurement                        |
| Muon System | Muon identification                                |

---

# 11. Importance for LHCb Physics

The Muon System is particularly important for channels containing muons.

## Example 1: \(B_s^0 \rightarrow \mu^+\mu^-\)

A particularly important rare decay is:

$$
B_s^0 \rightarrow \mu^+\mu^-
$$

The final state contains two muons:

```text
B_s⁰
 │
 └────→ μ⁺ + μ⁻
          │     │
          ▼     ▼
        Muon  Muon
       System System
```

Efficient muon identification is essential for selecting this signal and rejecting backgrounds.

---

## Example 2: \(B^0 \rightarrow K^{*0}\mu^+\mu^-\)

Another important decay is:

$$
B^0 \rightarrow K^{*0}\mu^+\mu^-
$$

Here the final state contains two muons and hadrons.

This type of decay is important for studying:

* Rare flavour-changing processes
* Electroweak interactions
* CP violation
* Tests of the Standard Model
* Indirect searches for New Physics

---

# 12. Muon System and Trigger

The Muon System also provides important information for event selection.

Historically, fast muon information was particularly useful for hardware-based trigger systems.

A simplified traditional trigger concept is:

```text
Collision
   │
   ▼
Hardware Trigger
   │
   ├── Reject
   │
   ▼
Software Trigger
   │
   ▼
Storage
```

With LHCb Upgrade I, the trigger architecture changed significantly.

The upgraded experiment uses:

$$
\boxed{\text{40 MHz readout + real-time software triggering}}
$$

The detector information, including Muon System information, can therefore be used in real-time reconstruction and event selection.

---

# 13. Punch-Through Background

An important limitation is that hadrons are not always completely stopped by the calorimeter.

Some high-energy hadrons can reach the Muon System:

$$
\boxed{\text{Hadron punch-through}}
$$

For example:

```text
Hadron
  │
  ▼
HCAL
  │
  │  Hadronic shower
  │
  │       some component
  │              │
  └──────────────┼──────→ Muon System
                 ●
```

Therefore, Muon identification must distinguish genuine muons from hadronic backgrounds.

This requires good:

* Detection efficiency
* Spatial resolution
* Timing performance
* Pattern recognition
* Track matching

---


# 17. Muon System vs. RICH

The two systems both contribute to particle identification, but they use very different physical principles.

|                     | RICH                                  | Muon System                          |
| ------------------- | ------------------------------------- | ------------------------------------ |
| Main purpose        | Particle identification               | Muon identification                  |
| Typical separation  | $\pi/K/p$                             | $\mu$ vs. non-$\mu$                  |
| Physical principle  | Cherenkov radiation                   | Penetration + gas detector response  |
| Detector technology | Cherenkov radiator + photon detection | Gas detectors                        |
| Position            | Central/downstream detector           | Far downstream                       |
| Key physics         | Particle velocity                     | Particle penetration and hit pattern |

A simple rule is:

$$
\boxed{\text{RICH: "What kind of charged particle is it?"}}
$$

while:

$$
\boxed{\text{Muon System: "Is this penetrating particle a muon?"}}
$$

---

# 18. Key Physical Picture

The entire concept can be summarized as:

```text
                   Collision
                       │
                       ▼
               Charged particle
                       │
                       ▼
                Tracking system
                       │
                       ▼
                   Magnet
                       │
                       ▼
                     RICH
                       │
                       ▼
                     ECAL
              ┌────────┴────────┐
              │                 │
          e / γ shower      other particles
              │                 │
              ▼                 ▼
            ECAL              HCAL
                                │
                         hadronic shower
                                │
                                ▼
                        ─────────────
                                │
                                ▼
                         MUON SYSTEM
                                │
                                ▼
                       Muon candidates
```

The essential physical difference is:

```text
Hadron:
strong interaction
       ↓
hadronic shower
       ↓
energy deposited in HCAL
       ↓
usually does not reach Muon System

Electron:
Bremsstrahlung
       ↓
electromagnetic shower
       ↓
energy deposited in ECAL
       ↓
usually does not reach Muon System

Muon:
no strong interaction
       ↓
mainly ionization
       ↓
gradual energy loss
       ↓
penetrates calorimeters
       ↓
reaches Muon System
```

---

# 19. Summary

The most important points about the LHCb Muon System are:

1. **The Muon System is located at the downstream end of LHCb.**

2. Its primary purpose is **muon identification**.

3. Muons are leptons and **do not participate in the strong interaction**.

4. Hadrons such as $\pi$, $K$, and $p$ can produce **hadronic showers** in the calorimeter.

5. Electrons can produce **electromagnetic showers** through Bremsstrahlung and pair production.

6. Muons mainly lose energy through **ionization**, allowing them to penetrate much further through matter.

7. The Muon System is therefore designed to detect particles that survive the calorimeters.

8. It consists of multiple muon stations, traditionally denoted:

$$
M1,\ M2,\ M3,\ M4,\ M5
$$

9. The system mainly uses **gas detectors**, including technologies such as MWPCs and GEMs.

10. Multiple stations provide a **hit pattern** that can be matched to reconstructed tracks.

11. Muon identification is not perfect because **hadron punch-through** can create background hits.

12. Muon information is important for both **physics analyses and event selection/triggering**.

13. Important LHCb physics channels containing muons include:

$$
B_s^0\rightarrow\mu^+\mu^-
$$

and

$$
B^0\rightarrow K^{*0}\mu^+\mu^-.
$$

14. Increasing luminosity leads to higher:

$$
\text{rate},\quad
\text{occupancy},\quad
\text{radiation},\quad
\text{data volume}
$$

which creates major challenges for future upgrades.

---
