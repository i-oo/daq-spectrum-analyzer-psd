# daq-spectrum-analyzer-psd

> C program for automated power spectral density (PSD) acquisition from the Stanford Research Systems SR785 dual-channel signal analyzer over GPIB.

![Language](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Interface](https://img.shields.io/badge/GPIB%20%2F%20VISA-instrument%20control-gray?style=flat)
![Domain](https://img.shields.io/badge/Domain-Signal%20Analysis%20DAQ-lightgray?style=flat)

## What It Does

Automates frequency-domain measurements from the SR785 spectrum analyzer — configuring measurement parameters, triggering sweeps, and pulling PSD data over GPIB into structured output files. Written in 2020, refined through 2022.

The SR785 is a dual-channel dynamic signal analyzer capable of measurements from DC to 102.4 kHz. This code removes the need for manual sweep configuration and export, enabling repeatable, scriptable noise characterization runs.

## Transferable Skills

This project demonstrates:

- **Signal acquisition and parsing** — reading structured numeric data from an instrument over a serial-style protocol is the same fundamental pattern as parsing log streams, SNMP traps, or API responses in IT systems
- **Frequency-domain analysis concepts** — understanding power spectral density, noise floors, and signal characterization translates directly to anomaly detection, where you distinguish signal from noise in time-series data (network traffic, security events)
- **Automated measurement pipelines** — configuring, triggering, and collecting from a remote device maps to how monitoring agents, SIEM collectors, and telemetry pipelines work
- **C programming under real constraints** — timing, buffer management, and communication reliability in a lab instrument environment

## Hardware

- **Instrument:** Stanford Research Systems SR785 Dynamic Signal Analyzer
- **Interface:** GPIB via National Instruments VISA
- **Language:** C (NI-VISA library)

## Context

Part of the same multi-instrument noise measurement pipeline as [`daq-agilent-psu`](https://github.com/i-oo/agilent_PSU) and [`daq-keithley-iv`](https://github.com/i-oo/Keithley2600_daq). The SR785 captured noise spectra while the PSU and SMU biased the device under test.
