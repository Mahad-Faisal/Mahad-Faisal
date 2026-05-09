<h1 align="center">Mahad Faisal</h1>

<h3 align="center">
Embedded Firmware Engineer | RTOS | Motor Control | Battery Estimation | Edge AI
</h3>

Computer Engineering student at Drexel University focused on low-level embedded systems, real-time firmware, motor-control platforms, embedded estimation algorithms, and safety-critical firmware architecture.

Previously worked as an Embedded Firmware Engineer Co-op at Rheem Manufacturing developing inverter firmware, RTOS-based HVAC platforms, and embedded communication systems on Renesas RX/RA MCUs.

---

## Current Work

### Adaptive Battery Management System (RA8M1 + FreeRTOS)
- Building an embedded Adaptive Dual Extended Kalman Filter (ADEKF) battery estimator on the Renesas EK-RA8M1 (Cortex-M85)
- Real-time electrothermal battery plant simulation running on ESP32 communicating over CAN 2.0
- 5-state electrothermal 2RC ECM with coupled thermal dynamics
- Real-time estimation of:
  - State of Charge (SoC)
  - RC polarization voltages
  - thermal states
  - adaptive parameter correction
- Embedded telemetry + UART logging infrastructure for HIL validation
- HPPC validation:
  - 5.31 mV RMS @ 25°C
  - 6.95 mV RMS @ 10°C
  - 8.98 mV RMS @ 0°C
- Corrected real UDDS validation:
  - 10.94 mV raw RMS
  - 10.21 mV bias-corrected RMS

---

## Professional Embedded Firmware Experience

### Embedded Firmware Engineer Co-op — Rheem Manufacturing
**Jan 2025 – Sep 2025**

#### RX26T 3-Phase ACIM Inverter Firmware
- Sole firmware developer on a safety-critical 3-phase ACIM inverter platform for HVAC furnace inducer control
- Performed full low-level RX26T bring-up:
  - clocks
  - pin mux
  - ADC
  - PWM
  - POEG
  - deadtime
  - linker memory restructuring
- Reduced EMI-induced production resets from 45% → 1.5% through firmware mitigation and root-cause analysis of ADC polling instability under electrical noise
- Integrated external PWM capture and RPM command translation logic
- Ported Renesas FOC motor-control firmware across MCU families and adapted PMSM-oriented firmware for ACIM operation
- Implemented thermistor-based IPM thermal monitoring using Steinhart-Hart characterization and interrupt-driven ADC acquisition
- Developed dual-flash boot/fallback architecture for inverter recovery and field reliability

#### Commercial HVAC RTOS Migration
- Led bare-metal → FreeRTOS migration for commercial HVAC control platforms
- Re-architected superloop firmware into deterministic task/timer scheduling using semaphores and message passing
- Tuned ISR latency, stack/heap usage, and task scheduling under real electrical-load conditions using Tracealyzer
- Root-caused UART contention issues affecting motor operation

#### Embedded Communications + Internal Tooling
- Implemented proprietary HVAC communication stacks over SCI UART with interrupt-driven callbacks and timing-sensitive transmit control
- Worked on RAM optimization and reusable firmware templates for additional commercial platforms
- Built internal Python tooling converting Excel datasets into firmware-ready bytestreams with CRC insertion, endian conversion, structured headers, and round-trip parsing support

---

## Embedded Systems Interests
- Zephyr RTOS
- FreeRTOS
- Renesas RA/RX platforms
- ADC/DMA pipelines
- UART/SPI/I2C/CAN
- Motor control and inverter firmware
- Embedded signal processing
- State estimation and Kalman filtering
- Cortex-M85 / Arm Helium
- CI/CD for embedded firmware
- Safety-critical embedded systems
- Hardware bring-up and low-level MCU initialization

---

## Technologies
C • C++ • Python • MATLAB • FreeRTOS • Zephyr • CAN 2.0 • Git • CMake • Ninja • Jenkins • Linux • Renesas e² studio

---

## Current Open Source Work
- Contributing to Zephyr RTOS
- Improving Renesas RA8M1 board/sample support
- Exploring Cortex-M85 CMSIS-DSP and Helium acceleration paths
- Working on embedded CI/CD workflows and firmware validation infrastructure

---

📫 mahad.faisal@gmail.com
