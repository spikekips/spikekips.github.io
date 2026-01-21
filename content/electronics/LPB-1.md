---
title: "LPB-1"
date: 2026-01-19T12:00:00-06:00
draft: false
unsafe: true
#layout: single
---

The LPB-1(Linear Power Booster) is a guitar pedal that acts as a pre-amp

## Equations
### Starting Values
V~CC~ = 9V

V~BE~ = .7V

h~fe~ = 300

R1 = 1MΩ

R2 = 100kΩ

RC = 10kΩ

RE = 390Ω

### Calculated Values
$V_{B} \cong \frac{R2}{R1+R2}*V_{CC} = \frac{R2}{R1+R2}*V_{CC} = 818mV$

$V_{E} = V_{B} - V_{BE} = 818mV - 700mV = 118mV$

$I_{E} = \frac{V_{E}}{RE} = \frac{118mV}{390Ω} = 303uA$

$I_{C} \cong I_{E} = 303uA$

$V_{C} = V_{CC}-I_{C} = 9-303uA = 5.97V$

$I1 = \frac{V_{CC}-V_{B}}{R1} = \frac{9V-818mV}{1MΩ} = 8.18uA$

$I2 = \frac{V_{B}}{R2} = \frac{818mV}{100kΩ} = 8.18uA$

$R_{B} = \frac{R1xR2}{R1+R2} = \frac{1MΩx100kΩ}{1MΩ+100kΩ} = 90uΩ$

$I_{B} = \frac{V_{B}}{R_{B}+1x300xRE} = \frac{818mV}{90uΩ+1x300x390Ω} = 1.008uA \cong \frac{I_{C}}{h_{fe}}$ 

$V_{CE} = V_{CE} - V_{E} = 5.85$

### Q-Point Calculations

$V_{CE}$ Ideal Cutoff $= V_{CC}  = 9V$ 

$I_{C}$ Ideal Saturation $= \frac{V_{CC}}{RC} = \frac{9V}{10k\Omega} = 900uA$

$I_{C (max)}$ Max Saturation $= \frac{V_{CC}-V_{RE}}{RC} = \frac{9V-118mV}{10k\Omega} = 888uA$

$V_{C (min)}$ Min Cutoff $= V_{RE} = 118mV$

$V_{CEQ} = V_{C} = 5.97V$

$I_{CQ} = I_{C} - \frac{V_{CEQ}}{I_{C}} = 900uA - \frac{5.97V}{10k\Omega} = 303uA$
