---
title: "Logic Gates"
date: 2026-01-30T00:00:00-06:00
draft: false
unsafe: true
#layout: single
---

## Transistor AND Gates
And Gates are a way to determine if two inputs are both on. If both inputs are on then the output is on.

|x|y|output|
|-|-|------|
|0|0|0|
|1|0|0|
|0|1|0|
|1|1|1|
{.logicTable}

![AND Gate](/kiCad/images/ANDGate.png 'elecPic')

When both transistors are turned on then current flow from the collector to emitter on both transistors allowing the diode to turn on.

## Transistor NAND Gate
|x|y|output|
|-|-|------|
|0|0|1|
|1|0|1|
|0|1|1|
|1|1|0|
{.logicTable}

![NAND Gate](/kiCad/images/NANDGate.png 'elecPic')

In a NAND gate the logic output flows only when the AND portion of the circuit is off. If any input is off in the circuit then the logic voltage output is high (1). When both inputs are on then logic voltage is low (0). 

## OR Gate
|x|y|output|
|-|-|------|
|0|0|0|
|1|0|1|
|0|1|1|
|1|1|1|
{.logicTable}

![OR Gate](/kiCad/images/ORGate.png 'elecPic')

## NOR Gate
|x|y|output|
|-|-|------|
|0|0|1|
|1|0|0|
|0|1|0|
|1|1|0|
{.logicTable}

![NOR Gate](/kiCad/images/NORGate.png 'elecPic')

## NOT Gate
|x|output|
|-|------|
|0|1|
|1|0|
{.logicTable}

![NOT Gate](/kiCad/images/NOTGate.png 'elecPic')

## XOR Gate
|x|y|output|
|-|-|------|
|0|0|0|
|1|0|1|
|0|1|1|
|1|1|0|
{.logicTable}

### XOR 1
![XOR Gate 1](/kiCad/images/XORGate1.png 'elecPic')

If both are on then current flow to ground 0. This means the transitro Q13 won't turn on so the diode will have no current flow.

If only one input is on then current flows through the diode

If there is no input then no current flows but Q13 does turn on.

### XOR 2
![XOR Gate 2](/kiCad/images/XORGate2.png 'elecPic')

Same as XOR 1 but has output that can be sent to other things

Has a not gate to invert the inversion without the inversion it'd end up being an XNOR Gate.

## XNOR Gate
|x|y|output|
|-|-|------|
|0|0|1|
|1|0|0|
|0|1|0|
|1|1|1|
{.logicTable}

![XNOR Gate](/kiCad/images/XNORGate.png 'elecPic')
