# Speeds and Feeds
#note

**Cutting Speed**  - relative velocity between workpiece and tool (surface $\pu{ft/min}=\pu{sfm}$) or ($\pu{m/min}$)

**Spindle Speed** - tool spindle (mill, drill) or workpiece (lathe) speed $(\pu{rpm})$

**Feed or Feed Rate** - how fast the tool is plunging into the material in $x$ or $y$ axes ($\pu{in/min}$ or $\pu{ipm}$) (mill) or ($\pu{in/rev}$ or $\pu{ipr}$) (lathe)

**Depth of Cut** - $z$ axis plunge $(\pu{in})$ or $(\pu{mm})$

## Speeds
We can determine spindle speed or cutting speed by knowing one or the other term
- Typically cutting speed is provided for tool & workpiece materials, and spindle speed is calculated for machine control
To determine spindle speed $S$ in ($\pu{rpm}$):
$$
\boxed{
S= \frac{V \cdot \pu{12 \frac{in}{ft}}}{D\times \pi}=\frac{V \cdot 3.82}{D} \ \text{or} \ S= \frac{V \cdot \pu{1000 \frac{mm}{m}}}{D\times \pi}}
$$

Where the following units should be used:
- $S$ = spindle speed $(\pu{rpm})$
- $V$ = cutting speed $(\pu{ft/min})$ or $(\pu{m/min})$
- $D$ = workpiece or tool diameter $(\pu{in})$ or $(\pu{mm})$

## Feeds
How fast the tool advances across the part
- On a lathe, **inches-per-revolution** ($\pu{ipr})$ or $(\pu{mm/rev})$
- On a mill, **inches-per-minute** $(\pu{ipm})$ or $(\pu{mm/min})$

For turning, feed rate can be directly applied, but needs to be calculated for mill/drill operations.

$$
\mathrm{Fm} = S \cdot f_t \cdot n_t
$$

Where we have:
- $\mathrm{Fm}$ = feed rate $(\pu{in/min})$ or $(\pu{mm/min})$
- $S$ = cutter RPM
- $f_t$ = feed per tooth $(\pu{in/t})$ or $(\pu{mm/t})$
- $n_t$ = number of teeth or flutes on cutter


## Calculating Speeds and Feeds

### Example 1: Determine Speeds and Feeds for a $1/4\ \pu{in}$ HSS drill cutting **6061-T6 aluminum**

[**Relevant URL**](http://www.carbidedepot.com/formulas-drills-speeds.htm)

##### **1:** Determine speed first
250 SFPM is the midpoint of the suggested 

Using imperial units:

$$S=\frac{\pu{250 ft/min} \cdot 3.82}{\pu{0.25in}} = \pu{3820 rpm}$$

##### **2:** Now calculate feed rate

Most CNC machines require feed to be in inches per minute $(\pu{ipm})$, but the table gives inches **per revolution** ($\pu{ipr})$. To fix this, we need to multiply the spindle speed $S$ by the feed per revolution from the table.

$$\mathrm{Fm} = (\pu{3820 rpm}\cdot\pu{0.006 in/rev})\cdot \pu{1 tooth} = \pu{22.9 ipm}$$


### Example 2: Determine Speeds and Feeds for a **3-flute,** $1/2\ \pu{in}$ carbide endmill cutting **6061-T6 aluminum**

[**Relevant URL**](https://www.harveytool.com/resources/general-machining-guidelines##non-ferrous)

##### **1:** Determine speed

Targeting $\pu{1000 SFM}$, we have:

$$S = \frac{\pu{ 1000 ft/min}\cdot 3.82}{\pu{0.5 in}}=\pu{7640 rpm}$$
##### **2**: Determine Feed

From the chart, we have $f_t=\pu{0.004 ipt}$.

***In general, the more teeth or flutes we have, the higher feed we can run at.***

$$\mathrm{Fm}=\pu{7640 rpm}\cdot\pu{0.004 in/rev} \cdot \pu{3 teeth} = \pu{91.76 ipm}$$

