# Changelog

## v2 - Corrected datasheet reference

- Corrected STC Vmp from calculated `40.98 V` to datasheet **`41.00 V`**.
- Kept datasheet Imp = **17.69 A**, Voc = **49.20 V**, Isc = **18.74 A**.
- Nominal STC power remains **725 W**.
- Documented the 0.29 W (0.040%) datasheet rounding difference.
- Added an explicit **25°C** sampling row.
- Recalculated all 500 and 1000 W/m² tables.
- Rebuilt all I-V, P-V, Vmp, Imp, Pmp, and power-loss graphs.
- Marked 80°C and 90°C as extrapolated because datasheet operating temperature ends at +70°C.
- Clarified that 500 W/m² curves are modeled estimates, not manufacturer numerical curve data.
