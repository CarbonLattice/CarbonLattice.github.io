+++
title = "Boron Dev Boards"
date = 2025-08-17
draft = false

[taxonomies]
categories = ["Electrical-Engineering"]
tags = ["stm32", "devboards", "kicad"]

[extra]
toc = true
+++

## Introduction

The Boron series of dev boards is my attempt to learn and practice KiCad and PCB design while (hopefully) also making something that’s at least somewhat useful.

## Inspiration

The inspiration behind this project is fairly simple: I think the dev boards produced by STM and other manufacturers, while nice, are often too basic and don’t take advantage of the more interesting features included in the MCUs themselves.

I first came to this conclusion when working on another project where I wanted to experiment with CAN and CAN loopback. The STM32F446 I was using included two CAN peripherals — but none of the additional passive or active components needed to actually make use of them.  

Other missing features I found odd included:  
- Various crystals for better precision  
- Standard connectors  
- USB-C support  

So I set out to come up with a potential solution: design a board that has those extra peripheral, passive, and active parts already included.

## The Lineup So Far

Here are the MCUs I’ve chosen so far:

### STM32G0B0KE

This is the smallest (and hopefully simplest) option. My plan is to include only the most basic peripherals while keeping the board size very small — around the size of a Teensy LC or 4.0.  

A potential use case would be as the MCU for custom keyboards, which currently most often use Arduino Nano or RP2040. That said, this may be less practical, since existing keyboard firmware expects USB programming via DFU — something I don’t think this chip currently supports.

### STM32F205RE

This would (hopefully) be the next step up in the lineup. It wasn’t chosen for any specific reason beyond the fact that it uses an M33 core instead of the more common M4 core (which is what most third-party dev boards use).  

It also includes CAN and two USB peripherals, making it a solid mid-range option.

### STM32H563VI

This is the higher-end model, and it includes a lot of interesting features:  
- USB PD  
- CAN FD  
- Ethernet  
- DCMI/PSSI port for connecting cameras  

The camera interface is particularly exciting — running basic computer vision on low-power MCUs is something I find fascinating and could see direct applications for.

### STM32N657X0

This is the last one in the lineup, and definitely the least likely for me to attempt right now. It’s based on one of the newest Cortex cores and includes a lot of advanced features that I don’t currently understand well enough to implement.

## Conclusion

That’s it for the introduction to this project. Honestly, it’s way above what I would currently consider myself capable of — but that’s often how I learn, and how I push myself forward. Even if it feels “impossible” now, the process itself is worth it.
