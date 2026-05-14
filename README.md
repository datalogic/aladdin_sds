# Datalogic Aladdin SDS
## Design Document

**Version:** 1.3.0 
**Last Saved:** 14/05/2026

---

## Overview

The **Aladdin SDS (Silent Deploy Service)** is a service running on the **HOST** to detect, configure, and upgrade Datalogic **HHS** and **FRS** devices. It also provides communication interfaces with the **Datalogic Connect** system.

---

## Supported Device

| Category | Product | Interface | Logs | Beep | Reset | Custom Config | FW Upgrade |
|--------|---------|-----------|------|------|-------|---------------|------------|
| Gryphon | Gryphon 46xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Gryphon 45xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Gryphon 42xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Gryphon 41xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Gryphon 44xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Gryphon 43xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Gryphon | Base Chargers | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan 25xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan 24xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan 22xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan 21xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan QW25 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan QW24 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | QuickScan QW21 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| QuickScan | Base Chargers | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 96x0 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 95x1 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 95x0 | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 91xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 93xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | PowerScan 71xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| PowerScan | Base Chargers | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 900i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 1500i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 3x10 / 3x50i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 36 / 3700i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 93 / 9400i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 9550i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 9800i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| Magellan | Magellan 96 / 9900i | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |
| OEM Scan Engine | GFS45xx | USB-COM / USB-OEM | ✔ | ✔ | ✔ | ✔ | ✔ |

---

**Legend:** ✔ Supported | ❌ Not Supported

---

## Aladdin SDS Configuration

(TBD)

## MQTT Interface

(TBD)

## HTTP Interface

(TBD)

## WebSocket Interface

(TBD)

## Notification

(TBD)

---

**Datalogic INTERNAL**
