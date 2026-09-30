# Luminosity（亮度）

## 1. 什么是亮度？

在高能物理中，**亮度（Luminosity）**描述的是：

> 两束粒子束发生碰撞的“能力”有多强。

它本身不是碰撞事件数，而是决定单位时间内能够产生多少碰撞事件。

核心关系：

$$
\boxed{R=L\sigma}
$$

其中：

* $L$：瞬时亮度（instantaneous luminosity）
* $\sigma$：过程的反应截面（cross section）
* $R$：该过程的事件率（event rate）

---

## 2. 瞬时亮度（Instantaneous Luminosity）

瞬时亮度定义为：

$$
\boxed{
L=\frac{dN_{\rm events}/dt}{\sigma}
}
$$

单位通常为：

$$
\mathrm{cm^{-2}s^{-1}}
$$

例如：

$$
L=10^{34}\ \mathrm{cm^{-2}s^{-1}}
$$

意味着在这个亮度下，一个截面为 $\sigma$ 的过程，其事件率由

$$
R=L\sigma
$$

决定。

### 直觉

可以把：

* **碰撞能量**理解为“能不能产生某种粒子”
* **亮度**理解为“能产生多少次”

所以：

$$
\boxed{
\text{Energy} \rightarrow \text{what can be produced}
}
$$

$$
\boxed{
\text{Luminosity} \rightarrow \text{how many can be produced}
}
$$

---

# 3. 事件率与截面

由

$$
R=L\sigma
$$

可以得到：

$$
\boxed{
R=\frac{dN}{dt}
}
$$

因此：

$$
\frac{dN}{dt}=L\sigma
$$

例如：

$$
L=10^{34}\ \mathrm{cm^{-2}s^{-1}}
$$

假设某过程：

$$
\sigma=1\ \mathrm{pb}
$$

由于：

$$
1\ \mathrm{pb}=10^{-36}\ \mathrm{cm^2}
$$

所以：

$$
R=10^{34}\times10^{-36}
=10^{-2}\ \mathrm{s^{-1}}
$$

即：

$$
R=0.01\ \mathrm{Hz}
$$

平均约每 $100$ 秒产生一个这样的事件。

---

# 4. 积分亮度（Integrated Luminosity）

实验运行一段时间后，亮度会随时间变化：

$$
L=L(t)
$$

因此不能简单使用一个固定的 $L$。

定义积分亮度：

$$
\boxed{
\mathcal L_{\rm int}
=
\int L(t)\,dt
}
$$

它表示整个数据采集期间累计获得了多少“碰撞能力”。

常用单位：

* $\mathrm{fb^{-1}}$
* $\mathrm{pb^{-1}}$
* $\mathrm{ab^{-1}}$

---

# 5. 积分亮度与事件数

从

$$
\frac{dN}{dt}=L(t)\sigma
$$

两边积分：

$$
N=\int L(t)\sigma\,dt
$$

如果 $\sigma$ 不随时间变化：

$$
N=\sigma\int L(t)\,dt
$$

因此：

$$
\boxed{
N=\sigma\mathcal L_{\rm int}
}
$$

这是高能物理中非常重要的公式。

---

# 6. 一个常见单位换算

假设：

$$
\sigma=1\ \mathrm{pb}
$$

数据量：

$$
\mathcal L_{\rm int}=100\ \mathrm{fb^{-1}}
$$

因为：

$$
1\ \mathrm{fb^{-1}}=1000\ \mathrm{pb^{-1}}
$$

所以：

$$
100\ \mathrm{fb^{-1}}
=
10^5\ \mathrm{pb^{-1}}
$$

于是：

$$
N
=
1\ \mathrm{pb}
\times
10^5\ \mathrm{pb^{-1}}
$$

得到：

$$
\boxed{N=10^5}
$$

也就是说，理论上期望产生约：

$$
100\,000
$$

个事件。

注意：这是**产生的事件数**，实际分析中还要考虑探测效率、触发效率、重建效率、选择效率等。

---

# 7. 实际观测事件数

实际分析中：

$$
N_{\rm observed}
\neq
\sigma\mathcal L_{\rm int}
$$

因为不是所有产生的事件都能被探测和选择出来。

通常写成：

$$
\boxed{
N_{\rm obs}
=
\sigma\mathcal L_{\rm int}
\epsilon
}
$$

其中：

$$
\epsilon
=
\epsilon_{\rm trigger}
\epsilon_{\rm reconstruction}
\epsilon_{\rm selection}
\cdots
$$

所以：

$$
\boxed{
N_{\rm obs}
=
\sigma\mathcal L_{\rm int}\epsilon
}
$$

---

# 8. 为什么亮度越高越好？

由：

$$
R=L\sigma
$$

可以看到：

$$
R\propto L
$$

亮度越高，单位时间内产生的碰撞事件越多。

因此更高的 luminosity 意味着：

* 更多数据
* 更小的统计误差
* 更容易研究小截面的稀有过程
* 更高的 discovery sensitivity

统计误差通常近似满足：

$$
\delta N_{\rm stat}\sim\sqrt N
$$

相对统计误差：

$$
\frac{\delta N}{N}
\sim
\frac{1}{\sqrt N}
$$

所以：

$$
\boxed{
N\uparrow
\Rightarrow
\text{statistical uncertainty}\downarrow
}
$$

---

# 9. 亮度与稀有过程

假设一个过程的截面非常小：

$$
\sigma_{\rm rare}\ll\sigma_{\rm common}
$$

即使过程允许发生，它的事件率仍然可能非常低：

$$
R=L\sigma_{\rm rare}
$$

提高 $L$ 可以增加稀有过程的事件数：

$$
N_{\rm rare}
=
\sigma_{\rm rare}\mathcal L_{\rm int}
$$

因此研究 rare decay、稀有新粒子等过程时，大积分亮度非常重要。

---
# Bunch（束团）

## 1. 什么是 Bunch？

在加速器中，粒子并不是均匀地分布在整个环上，而是被组织成一个个**束团（Bunch）**。

可以理解为：

$$
\boxed{
\text{Particle}
\rightarrow
\text{Bunch}
\rightarrow
\text{Beam}
}
$$

即：

* **Particle**：单个粒子
* **Bunch**：一群在空间上聚集在一起的粒子
* **Beam**：沿加速器运行方向运动的大量 bunch

例如 LHC 中，proton 被分成很多 bunch，每个 bunch 内包含大量 proton。

---

## 2. 为什么要把粒子分成 Bunch？

加速器利用 RF（radio-frequency）系统让粒子集中在特定的时间和空间位置。

RF cavity 会产生周期性的电场，只有满足合适条件的粒子才能稳定地被加速。

因此粒子会被“聚集”到一个个 **RF bucket** 中：

$$
\boxed{
\text{RF system}
\rightarrow
\text{RF buckets}
\rightarrow
\text{particle bunches}
}
$$

所以 bunch 不是简单地把粒子“装在一起”，而是由加速器的 RF 结构形成的。

---

## 3. 两束 Beam 如何发生碰撞？

LHC 中有两束反向运动的 proton beam：

```text
Beam 1
→ → → → → → → → →

                IP
                ●
                ↑
                ↓

← ← ← ← ← ← ← ← ←
Beam 2
```

当两个 beam 中的 bunch 在 **Interaction Point (IP)** 相遇时，就可能发生 proton-proton collision。

因此：

$$
\boxed{
\text{Bunch crossing}
\rightarrow
pp\ interactions
\rightarrow
\text{events}
}
$$

这里要注意：

> 一次 bunch crossing 不一定只发生一个 pp interaction。

一次 crossing 中可能同时发生多个 pp interactions，这就是 **pileup**。

---

## 4. Bunch Crossing

当两个反向运动的 bunch 在 IP 相遇时，称为一次 **bunch crossing**。

可以简单表示：

```text
Bunch 1        → → → ●
                     │
                     │ IP
                     │
Bunch 2        ← ← ← ●
```

如果两个 beam 中有很多 bunch，那么随着它们绕环运动，会不断发生 bunch crossings。

因此实验会持续产生碰撞事件。

---

## 5. 一个 Bunch 里有多少粒子？

一个 bunch 中包含大量粒子。

记每个 bunch 中的粒子数为：

$$
N_1,\quad N_2
$$

对于两个碰撞的 bunch：

* Beam 1 中有 $N_1$ 个粒子
* Beam 2 中有 $N_2$ 个粒子

两个 bunch 越“密”，发生相互作用的机会通常越大。

因此 luminosity 会与：

$$
N_1N_2
$$

有关。

---

## 6. Bunch 数量与 Luminosity

一个简化的 luminosity 公式：

$$
\boxed{
L\sim
\frac{f_{\rm rev}n_bN_1N_2}
{4\pi\sigma_x\sigma_y}
}
$$

其中：

* $f_{\rm rev}$：beam 绕环一周的频率
* $n_b$：bunch 数量
* $N_1,N_2$：两个 beam 中每个 bunch 的粒子数
* $\sigma_x,\sigma_y$：beam 在横向的尺寸

因此：

### Bunch 数量增加

$$
n_b\uparrow
\quad\Rightarrow\quad
L\uparrow
$$

### 每个 Bunch 的粒子数增加

$$
N_1,N_2\uparrow
\quad\Rightarrow\quad
L\uparrow
$$

### Beam 聚焦得更紧

$$
\sigma_x,\sigma_y\downarrow
\quad\Rightarrow\quad
L\uparrow
$$

所以 bunch 是理解 luminosity 的重要组成部分。

---

## 7. Bunch 与 Luminosity 的直觉

可以把 luminosity 想象成“单位时间内制造碰撞的能力”。

如果：

* bunch 更多
* 每个 bunch 中的粒子更多
* bunch / beam 更集中

那么两个 beam 相遇时产生 interaction 的机会就更多。

因此：

$$
\boxed{
\text{more bunches}
+
\text{more particles per bunch}
+
\text{tighter beam}
\Rightarrow
\text{higher luminosity}
}
$$

---

## 8. Bunch Crossing 与 Pileup

一次 bunch crossing 中可能发生多个 pp interactions。

例如：

```text
Bunch crossing
      │
      ├── pp interaction 1
      ├── pp interaction 2
      ├── pp interaction 3
      ├── pp interaction 4
      └── ...
```

如果平均每次 crossing 有 $\mu$ 个 pp interactions，则：

$$
\boxed{
\mu=\text{average number of interactions per bunch crossing}
}
$$

例如：

$$
\mu=30
$$

表示平均而言，每次 bunch crossing 中约有 30 个 pp interactions。

这就是 **pileup**。

---

## 10. Bunch 与 Pileup 的关系

提高 luminosity 通常意味着：

$$
L\uparrow
\Rightarrow
\text{interaction rate}\uparrow
\Rightarrow
\mu\uparrow
$$

因此高 luminosity 虽然能够带来更多数据，但也会导致更高的 pileup。

这也是实验中的一个重要 trade-off：

$$
\boxed{
\text{High luminosity}
\Rightarrow
\text{more statistics}
}
$$

但同时：

$$
\boxed{
\text{High luminosity}
\Rightarrow
\text{more pileup}
}
$$

Pileup 会使事件重建和分析更加复杂。

---

# 为什么 MVA 通常不使用 Mass？

在很多高能物理分析中，特别是通过 **mass fit** 提取 signal yield 的分析，会有意将 **mass** 从 MVA（BDT、Neural Network 等）的输入变量中排除。

核心原因：

$$
\boxed{
\text{避免 Mass Sculpting}
}
$$

---

## 1. MVA 和 Mass 的分工不同

理想情况下，希望两个步骤分别完成不同任务：

$$
\boxed{
\text{MVA}
\rightarrow
\text{区分 Signal / Background}
}
$$

$$
\boxed{
\text{Mass fit}
\rightarrow
\text{提取 Signal Yield}
}
$$

也就是说：

> MVA 判断“这个事件像不像 signal”，而 mass 用来判断“signal 出现在什么质量位置，以及有多少 signal”。

因此通常希望 MVA 不依赖 mass。

---

## 2. 什么是 Mass Sculpting？

如果 MVA 使用了 mass，或者使用了与 mass 强相关的变量：

$$
\text{MVA variables}
\leftrightarrow
m
$$

那么 MVA cut 可能会改变 background 的 mass distribution。
MVA 很容易学到：

> “mass 接近 signal mass 的事件更像 signal。”

于是 MVA selection 本身就会选择某个 mass 区域。
例如原来的 background 是平滑的：

```text
Events
  │\
  │ \
  │  \
  │   \
  │    \
  └──────────────→ mass
```

经过 MVA selection 后可能变成：

```text
Events
  │
  │       /\
  │      /  \
  │_____/    \____
  └──────────────→ mass
```

这个人为产生的局部结构称为：

$$
\boxed{\text{Mass Sculpting}}
$$

---

## 3. 为什么 Mass Sculpting 是问题？

很多分析最终通过 mass distribution 做 signal extraction：

$$
f(m)
=
N_S S(m)+N_B B(m)
$$

其中：

* $S(m)$：signal mass shape
* $B(m)$：background mass shape
* $N_S$：signal yield
* $N_B$：background yield

通常希望：

$$
B(m)
$$

是平滑、容易建模的。

如果 MVA selection 改变了 background 的 mass shape，就可能：

* 产生人为的 peak 或 structure
* 使 background model 变复杂
* 增加 mass fit 的不确定性
* 造成 signal yield 的偏差
* 甚至产生类似 signal 的假结构

因此希望：

$$
\boxed{
\text{MVA selection}
\not\rightarrow
\text{改变 background mass shape}
}
$$

---


## 5. 但不使用 Mass 也不代表一定没有 Sculpting

这是一个重要细节。

即使 MVA 不直接使用：

$$
m
$$

也可能使用与 mass 强相关的变量：

$$
x\leftrightarrow m
$$

例如：

* $p_T$
* decay time
* vertex variables
* impact parameter
* isolation
* topology variables

那么：

$$
x\rightarrow\mathrm{MVA}
$$

仍然可能间接导致：

$$
\mathrm{MVA}\leftrightarrow m
$$

从而产生 mass sculpting。

所以实际分析中需要检查：

$$
\boxed{
\text{MVA output vs. mass}
}
$$

以及 MVA selection 前后的 background mass shape。

---
# 两个相同中心值的高斯分布的平均宽度

## 1. 问题

假设有两个 Gaussian distribution：

$$
G_1(x)=G(x;\mu,\sigma_1)
$$

$$
G_2(x)=G(x;\mu,\sigma_2)
$$

两者具有相同的中心值：

$$
\mu_1=\mu_2=\mu
$$

它们按照比例：

$$
f_1,\qquad f_2
$$

混合，并且：

$$
f_1+f_2=1
$$

那么混合分布的平均宽度是多少？

---

# 2. 混合分布

总的概率密度为：

$$
\boxed{
f(x)=f_1G_1(x)+f_2G_2(x)
}
$$

由于两个 Gaussian 的中心相同：

$$
E_1[X]=E_2[X]=\mu
$$

因此混合分布的均值仍然是：

$$
\boxed{
E[X]=\mu
}
$$

证明：

$$
E[X]
=
\int x f(x)\,dx
$$

代入混合分布：

$$
E[X]
=
\int x
\left[
f_1G_1(x)+f_2G_2(x)
\right]dx
$$

利用积分的线性：

$$
E[X]
=
f_1\int xG_1(x)dx
+
f_2\int xG_2(x)dx
$$

所以：

$$
E[X]
=
f_1\mu+f_2\mu
$$

因为：

$$
f_1+f_2=1
$$

得到：

$$
\boxed{
E[X]=\mu
}
$$

---

# 3. 用方差定义宽度

Gaussian 的宽度就是标准差：

$$
\sigma=\sqrt{\mathrm{Var}(X)}
$$

方差定义为：

$$
\boxed{
\mathrm{Var}(X)
=
E[(X-\mu)^2]
}
$$

因此我们计算混合分布的方差：

$$
\mathrm{Var}(X)
=
\int (x-\mu)^2 f(x)\,dx
$$

代入：

$$
f(x)=f_1G_1(x)+f_2G_2(x)
$$

得到：

$$
\mathrm{Var}(X)
=
\int (x-\mu)^2
\left[
f_1G_1(x)+f_2G_2(x)
\right]dx
$$

利用积分的线性：

$$
\mathrm{Var}(X)
=
f_1
\int (x-\mu)^2G_1(x)dx
+
f_2
\int (x-\mu)^2G_2(x)dx
$$

---

# 4. 利用 Gaussian 的方差定义

对于第一个 Gaussian：

$$
\int (x-\mu)^2G_1(x)dx
=
\sigma_1^2
$$

对于第二个 Gaussian：

$$
\int (x-\mu)^2G_2(x)dx
=
\sigma_2^2
$$

因此：

$$
\mathrm{Var}(X)
=
f_1\sigma_1^2
+
f_2\sigma_2^2
$$

所以混合分布的标准差为：

$$
\boxed{
\sigma_{\rm eff}
=
\sqrt{
f_1\sigma_1^2
+
f_2\sigma_2^2
}
}
$$

这就是两个具有**相同中心值**的 Gaussian mixture 的等效宽度。

---

# 5. 为什么不是简单的加权平均？

容易想到：

$$
\sigma_{\rm naive}
=
f_1\sigma_1+f_2\sigma_2
$$

但这通常是错误的。

原因是：

> **宽度对应的是标准差，而方差是标准差的平方。**

方差是：

$$
\sigma^2=E[(X-\mu)^2]
$$

所以混合时首先应该对：

$$
\sigma^2
$$

进行加权：

$$
\sigma_{\rm eff}^2
=
f_1\sigma_1^2
+
f_2\sigma_2^2
$$

最后再开平方：

$$
\boxed{
\sigma_{\rm eff}
=
\sqrt{
f_1\sigma_1^2
+
f_2\sigma_2^2
}
}
$$


由于：

$$
\sigma_{\rm eff}^2
=
f_1\sigma_1^2+f_2\sigma_2^2
$$

它实际上是 $\sigma_1^2$ 和 $\sigma_2^2$ 的加权平均。

因此：

$$
\min(\sigma_1,\sigma_2)
\leq
\sigma_{\rm eff}
\leq
\max(\sigma_1,\sigma_2)
$$

也就是说，等效宽度一定处于两个宽度之间。



---

# 6. 如果两个中心值不同

如果：

$$
\mu_1\neq\mu_2
$$

那么公式会多出一项。

一般情况下：

$$
\boxed{
\sigma_{\rm mix}^2
=
f_1\sigma_1^2
+
f_2\sigma_2^2
+
f_1f_2(\mu_1-\mu_2)^2
}
$$

前两项来自各自 Gaussian 的内部宽度：

$$
f_1\sigma_1^2+f_2\sigma_2^2
$$

最后一项：

$$
f_1f_2(\mu_1-\mu_2)^2
$$

来自两个中心值之间的距离。

因此本题之所以简单，是因为：

$$
\boxed{\mu_1=\mu_2}
$$

使得：

$$
f_1f_2(\mu_1-\mu_2)^2=0
$$

最终得到：

$$
\boxed{
\sigma_{\rm eff}
=
\sqrt{
f_1\sigma_1^2+f_2\sigma_2^2
}
}
$$

---
# LHCb Working Groups 构成

LHCb 的物理分析组织主要包括 **Physics Analysis Working Groups (PAWG)**、**Physics Performance Working Groups (PPWG)**、**Projects** 和 **Task Forces**。

---

## 1. Physics Analysis Working Groups（PAWG）

PAWG 主要按照物理研究方向组织分析。

### B&Q — B and Quarkonia

研究：

* B physics
* Quarkonia（夸克偶素）
* 与 B 强子和 quarkonium 相关的衰变与性质

---

### B2CC / BnoC — B decays to Charmonia / B decays without Charm

研究 B 强子的相关衰变。

主要包括：

* **B2CC**：B decays to Charmonia
* **BnoC**：B decays without Charm


---

### B2OC — B decays to Open Charm

研究：

> B 强子衰变到 Open Charm 的过程。

例如：

$$
B\rightarrow DX
$$

其中 \(D\) 等属于 open-charm hadrons。

---

### Charm

研究 charm physics，包括：

* \(D\) 介子
* charm hadrons
* charm mixing
* charm CP violation
* charm decays

例如：

$$
D^0\rightarrow K^-\pi^+
$$

---

### IFT — Ions and Fixed Target

研究：

* Heavy-ion physics
* Fixed-target physics
* QCD
* 核物质相关物理

---

### QEE — QCD, Electroweak and Exotica

研究：

* QCD
* Electroweak physics
* Exotica
* 新粒子、新相互作用等

例如：

* \(W/Z\)
* QCD processes
* exotic particles

---

### RD — Rare Decays

研究稀有衰变（Rare Decays）。

典型例子：

$$
B_s^0\rightarrow\mu^+\mu^-
$$

以及其他 flavor-changing neutral current（FCNC）过程。

---

### SL — Semileptonic Decays

研究半轻子衰变（Semileptonic Decays）。

例如：

$$
B\rightarrow D\ell\nu
$$

$$
B\rightarrow D^*\ell\nu
$$

主要用于：

* CKM 参数测量
* Lepton Flavor Universality（LFU）
* \(b\rightarrow c\ell\nu\)
* \(b\rightarrow u\ell\nu\)

---

# 2. Physics Performance Working Groups（PPWG）

## PPWG

**Physics Performance Working Groups** 主要负责：

* 探测器性能
* 物理性能评估
* 相关性能研究
* 为物理分析提供性能方面的支持

与 PAWG 的区别可以简单理解为：

$$
\boxed{\text{PAWG}\rightarrow\text{研究具体物理问题}}
$$

$$
\boxed{\text{PPWG}\rightarrow\text{研究和评估物理性能}}
$$

---


# 3. LHCb Working Groups 总体结构

可以简单记成：

```text
LHCb
│
├── Physics Analysis Working Groups (PAWG)
│   │
│   ├── B&Q
│   │   └── B and Quarkonia
│   │
│   ├── B2CC / BnoC
│   │   └── B decays to Charm / without Charm
│   │
│   ├── B2OC
│   │   └── B decays to Open Charm
│   │
│   ├── Charm
│   │   └── Charm physics
│   │
│   ├── IFT
│   │   └── Ions and Fixed Target
│   │
│   ├── QEE
│   │   └── QCD, Electroweak and Exotica
│   │
│   ├── RD
│   │   └── Rare Decays
│   │
│   └── SL
│       └── Semileptonic Decays
│
├── Physics Performance Working Groups (PPWG)
│
├── Projects
│   │
│   ├── RTA
│   │   └── Real-Time Analysis
│   │
│   ├── DPA
│   │   └── Data Processing & Analysis
│   │
│   ├── Simulation
│   │
│   └── Computing
│
└── Task Forces
    │
    ├── StatML
    │   └── Statistics & Machine Learning
    │
    ├── AmAn
    │   └── Amplitude Analysis
    │
    ├── FT
    │   └── Flavour Tagging
    │
    └── Luminosity
```

---

# 4. 常见分析对应哪个 Working Group？

| 分析/物理过程                        | 主要 Working Group |
| ------------------------------ | ---------------- |
| \(D^0\rightarrow K^-\pi^+\)    | Charm            |
| \(D^0-\bar D^0\) mixing        | Charm            |
| \(B_s^0\rightarrow\mu^+\mu^-\) | RD               |
| \(B\rightarrow D\ell\nu\)      | SL               |
| \(B\rightarrow DX\)            | B2OC             |
| B → Charmonium                 | B2CC             |
| B decays without Charm         | BnoC             |
| Quarkonium                     | B&Q              |
| QCD                            | QEE              |
| Electroweak                    | QEE              |
| Exotic particles               | QEE              |
| Heavy-ion                      | IFT              |
| Fixed-target                   | IFT              |
| MVA / BDT / ML                 | StatML           |
| Amplitude Analysis             | AmAn             |
| Flavor Tagging                 | FT               |
| Luminosity measurement         | Luminosity       |

---
