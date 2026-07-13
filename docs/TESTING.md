# Testing and Evidence

## Experimental basis

The original controlled experiment used:

- an approximately 8 L enclosed chamber,
- fixed ABS extrusion,
- five treatment conditions,
- four trials per condition,
- two SGP41 sensor channels at different chamber locations,
- one BME688 sensor for secondary gas-response and environmental measurements,
- 900 s generation followed by 300 s recovery monitoring.

## Key engineering comparison

Measured mean values in the original chamber:

| Metric | 30 g active | 60 g passive |
|---|---:|---:|
| 900 s SGP41 response | 1.30 ± 0.21 log2-eq | 1.43 ± 0.20 log2-eq |
| 0-900 s cumulative response | 15.98 ± 3.14 log2-min | 18.19 ± 3.54 log2-min |

This comparison is an engineering observation in the tested chamber. It should not be described as universal superiority without validation across additional printer geometries.

## Full plots

See [`../data/combinedGasPlots.pdf`](../data/combinedGasPlots.pdf).

## Suggested independent validation

Testers should compare, at minimum:

1. existing filter only,
2. existing filter + OpenChamberFlow,
3. optional second-filter baseline.

Keep constant:

- filament and mass extruded,
- nozzle temperature,
- trial duration,
- sensor positions,
- carbon age and mass,
- chamber sealing,
- initial chamber conditions.

Record:

- endpoint response,
- cumulative response,
- spatial sensor difference,
- temperature and humidity,
- fan voltage/current,
- subjective noise,
- print-quality effects.

## Sensor limitation

SGP41 and BME688 devices are broadband comparative sensors. They do not replace analytical VOC concentration measurements or compound-specific analysis.
