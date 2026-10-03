# Basement Room: Wiring, Ventilation and Three-Level Control

A 19.6 m² basement room with a 2.0 m² bathroom, fully renovated. The renovation is ordinary; the engineering is the point: power wiring, lighting, ventilation with a duct heater, sensors, a distribution board, a control cabinet, and automation in three levels where the hardware always has the last word.

**Evgenii Zagorodskikh.** Contact: [LinkedIn](https://www.linkedin.com/in/evgenii-zagorodskikh-58671042a/).

## Three levels of control

| Level | What it is | What it may do |
|---|---|---|
| 0 — wiring | Contacts, relays and thermal cut-outs wired directly | Enables or blocks the heater; switches the lights from the push-buttons. Works with the controller and PC off. |
| 1 — OWEN PR200 + PRM | Programmable relay with an expansion module, hard logic | Runs ventilation, heater power and alarms on its own setpoints. Can only *permit* the heater, never force it on. |
| 2 — AI on a PC | Writes setpoints and commands to PR200 registers | Only requests. Limits it cannot exceed are held in the PR200; if it goes silent, the PR200 drops its commands. |

**Heater enable chain** (sheet 9). The contactor KM1 can pull in only when every link is closed at once: airflow present (SP1), both thermal cut-outs healthy (SK1 +50 °C auto, SK2 +100 °C manual reset), controller permission (DO4), no fire signal (K3). Four of the five links are hardware and work with the controller or PC hung or switched off.

**Lighting** (sheet 8). Three channels — entry, loft, work — on impulse relays KL1–KL3 in the distribution board. The push-buttons and the controller's interface relays KV1–KV3 are wired in parallel, so without the control cabinet the buttons work as ordinary switches. The controller reads each channel's state from the relay's auxiliary contact.

**AI link** (sheet 10). The PC writes setpoints and commands to PR200 registers and increments a heartbeat counter every 5 s. With no update for 30 s, the PR200 drops the AI's commands and runs on its own setpoints. Example limits the AI cannot exceed: supply air 14…24 °C, bathroom humidity switch-on 55…80 %, CO₂ switch-on 700…1200 ppm, heater ≤ 100 %; lighting is unrestricted.

**The one exception.** The air conditioner (Midea, local Wi-Fi) is controlled by the AI through the PC directly, not through the PR200. It is a self-contained unit and is not part of any interlock chain in this design.

## Stages

| Stage | Contents | Status |
|---|---|---|
| [2026-10-03-design](2026-10-03-design/) | Design kit: 16 sheets, interactive 3D model, cable schedule, specification, controller I/O | Published |
| Build and test | Installation as photographed, commissioning tests, the automation in detail | Planned |

## Status of the design

Working materials for procurement and installation, not a stamped design. The distribution board and incoming supply diagrams are to be agreed with the building management company and an electrical testing laboratory.

The kit was prepared with Claude (Anthropic) from my brief, sketches and photographs of the room.

## Licence

Drawings, text, data and the 3D model content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (full text: [`LICENSE-CC-BY-4.0.txt`](LICENSE-CC-BY-4.0.txt)) — free to use and adapt with attribution. Code of the 3D model page: [MIT](LICENSE). The embedded three.js library keeps its own MIT licence (Copyright 2010–2021 Three.js Authors).
