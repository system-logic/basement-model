# Stage 1 — Design kit (October 2026)

Room: 19.6 m² with a 2.0 m² bathroom; plan 6410 × 3250 mm. Working materials for procurement and installation, not a stamped design.

## Files

| File | What it is |
|---|---|
| [documentation.pdf](documentation.pdf) | 16 A4 landscape sheets, listed below |
| [3d-model.html](3d-model.html) | Interactive 3D model; download and open in a browser, works offline. Left mouse — rotate, right — pan, wheel — zoom, click — description of the element |
| [lists-and-specification.xlsx](lists-and-specification.xlsx) | Specification (totals recalculate), cable schedule, DB circuits, controller inputs and outputs |

## Sheets

1. General data
2. Power wiring route plan
3. Lighting plan
4. Sensors and low-voltage lines plan
5. Ventilation plan
6. DB single-line diagram
7. DB layout
8. Lighting control diagram
9. CC: power circuits and interlocks
10. CC: controller inputs and outputs
11. Control cabinet CC layout
12. Cable schedule
13–15. Specification
16. 3D model views

DB — distribution board; CC — control cabinet.

## Key decisions

- All cables run on the ceiling in an 18 cm black band, 90° turns only; drops on the walls in black flame-retardant PVC conduit; cable VVGng(A)-LS.
- Lighting: three channels — entry / loft (tracks T0, T3, 3000 K spots) / work (tracks T1, T2, 4000 K linear, ≈500–650 lx); push-button switch SW2 under the DB drives impulse relays.
- Ventilation Ø125: supply ≈100 m³/h with a G4 filter and a 1.5 kW duct heater, two exhausts ≈50 and ≈60 m³/h; airflow set by iris dampers; each fan has its own thresholds.
- Automation in three levels: 0 — wiring (heater enable chain, light buttons); 1 — OWEN PR200 + PRM, hard logic; 2 — AI on a PC, which only requests and can be switched off with no consequences. The PC can be added later and can be second-hand.
- Air conditioner above the control cabinet, controlled by the AI over Wi-Fi through the PC; two PoE cameras with no blind spots.
- DB — EKF two-door enclosure 580×490×165, 30 modules, mounted upside down: meter at the bottom right, meter window ≈1.4–1.6 m above the floor, conduit entries at the top.
- The entrance door opens outward, into the corridor; this is reflected on every plan and in the 3D model.

## To be confirmed on site

- Position of the heating pipes (taken from photographs, ±10–15 cm): it sets the location of socket S3 and the feeds to the control cabinet.
- Incoming cable grade and meter: per the management company's connection conditions.

## Cost

Estimated total, all sections: $3,812, as of 1 October 2026. All prices are estimates, converted from roubles at the Bank of Russia rate of 83.5588 RUB/USD on that date; sums are rounded to whole dollars. Not included: the PC, cameras and PoE switch (planned for later), air conditioner installation (to be confirmed), and items already bought — DB enclosure, QF1, meter, QF2, incoming cable, water heater.
