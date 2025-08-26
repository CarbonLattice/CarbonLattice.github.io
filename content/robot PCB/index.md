+++
title = "The Outline of a Skeleton of a Plan"
date = 2025-08-25
draft = false

[taxonomies]
categories = ["Electrical-Engineering"]
tags = ["stm32", "devboards", "kicad"]

[extra]
toc = true
+++

## THE PLAN

Based on my writings, you may or may not be able to tell that I don’t exactly know what I’m doing—and that I may or may not be a bit *special ed*. That’s definitely true in most cases. I usually have a hard time with both motivation and attention.

Part of my plan is to work on a robot main control board as a way of keeping my ADHD brain entertained, so the other part can focus on actually getting things done and learning.

Almost certainly this board will never be produced in any meaningful way, and the design will probably just sit on my GitHub to perish. But hey, hopefully I learn something from it—and maybe the experience can help me land a job, since I feel too stupid to go to higher education.

---

## Anyway

The plan is to use an **STM32 M7 core** with a bunch of sensors and connectivity options.

- **IIS2MDC** – 3-axis magnetometer from STMicro
- **LSM6DSV16X** – High-end IMU with accelerometers and gyroscopes
- **TESEO-LIV3FL** – GNSS module with a matching PCB-mount patch antenna

For communication:

- **2× CAN FD** lanes with matching transceivers
- **Bluetooth/Wi-Fi module** with a PCB antenna
- Basic **SBUS** and other connectors

My plan is to reach out to some people online and see if they have suggestions—maybe there’s something useful I can add.

---

## STM Supremacy

The reason so many parts are from STM is that they have good software support, solid documentation for hardware design, and their parts are commonly used.
