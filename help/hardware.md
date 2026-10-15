---
title: Hardware
permalink: /help/hardware
---

# Hardware: printers, drawers, scales and displays

## Without extra software

The POS prints receipts through the **browser** (any printer Windows knows, A4 or receipt printer).
The **customer display** opens as a second browser window (drag it to the second screen; allow pop-ups).
Barcode scanners that act as a keyboard work everywhere: PC, tablet, phone.

## With the Hardware Bridge (Windows)

Install **RposBridge** on the POS PC (free download). It runs as a Windows service and the POS reaches it at `http://127.0.0.1:9123`.
It drives:

* ESC/POS receipt and kitchen printers (USB, network, serial), with logo, QR code and barcode;
* cash drawers (through the printer or serial);
* VFD pole displays;
* serial scales (Essae, CAS, Mettler Toledo, Dibal, Avery, Bizerba, NCI and configurable protocols);
* serial scanners;
* label printers (ZPL, TSPL, EPL);
* local card terminals (bank EDCs, Ingenico, Verifone, PAX, Paytm / PhonePe ECR).

Set it up on the **Hardware Profile**: *Use Hardware Bridge*, bridge URL and token, and the device names configured in the bridge.
In Edge or Chrome, allow *local network access* for Business Central when asked.

See the Hardware Bridge README for installing the service and device configuration.
