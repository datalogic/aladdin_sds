# Datalogic Aladdin SDS
## Design Document

**Version:** 1.3.0 
**Last Saved:** 14/05/2026

---

## Overview

The **Aladdin SDS (Silent Deploy Service)** is a service running on the **HOST** to detect, configure, and upgrade Datalogic **HHS** and **FRS** devices. It also provides communication interfaces with the **Datalogic Connect** system.

---

## Supported Device

<table>
  <tr>
    <th>Category</th>
    <th>Product</th>
    <th>Interface</th>
    <th>Logs</th>
    <th>Beep</th>
    <th>Reset</th>
    <th>Custom Config</th>
    <th>FW Upgrade</th>
  </tr>

  <!-- Gryphon -->
  <tr>
    <td rowspan="7">Gryphon</td>
    <td>Gryphon 46xx</td>
    <td>USB-COM / USB-OEM</td>
    <td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td>
  </tr>
  <tr><td>Gryphon 45xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Gryphon 42xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Gryphon 41xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Gryphon 44xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Gryphon 43xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Base Chargers</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>

  <!-- QuickScan -->
  <tr>
    <td rowspan="8">QuickScan</td>
    <td>QuickScan 25xx</td>
    <td>USB-COM / USB-OEM</td>
    <td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td>
  </tr>
  <tr><td>QuickScan 24xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>QuickScan 22xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>QuickScan 21xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>QuickScan QW25</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>QuickScan QW24</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>QuickScan QW21</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Base Chargers</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>

  <!-- PowerScan (no merge requested, keep normal) -->
  <tr>
    <td rowspan="7">PowerScan</td>
    <td>PowerScan 96x0</td>
    <td>USB-COM / USB-OEM</td>
    <td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td>
  </tr>
  <tr><td>PowerScan 95x1</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>PowerScan 95x0</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>PowerScan 91xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>PowerScan 93xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>PowerScan 71xx</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Base Chargers</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>

  <!-- Magellan -->
  <tr>
    <td rowspan="8">Magellan</td>
    <td>Magellan 900i</td>
    <td>USB-COM / USB-OEM</td>
    <td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td>
  </tr>
  <tr><td>Magellan 1500i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 3x10/3x50i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 36/3700i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 93/9400i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 9550i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 9800i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>
  <tr><td>Magellan 96/9900i</td><td>USB-COM / USB-OEM</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td></tr>

  <!-- OEM -->
  <tr>
    <td>OEM Scan Engine</td>
    <td>GFS45xx</td>
    <td>USB-COM / USB-OEM</td>
    <td>✔</td><td>✔</td><td>✔</td><td>✔</td><td>✔</td>
  </tr>

</table>

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
