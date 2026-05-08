<h1 align="center">Mahad Faisal</h1>
<h3 align="center">
Embedded Firmware | RTOS | Motor Control | Battery Estimation | Edge AI
</h3>

Computer Engineering student at Drexel University focused on low-level embedded systems, real-time firmware, signal processing, and embedded estimation algorithms.

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

---

## Technologies
C • C++ • Python • MATLAB • FreeRTOS • Zephyr • CAN 2.0 • Git • CMake • Ninja • Jenkins • Linux • Renesas e² studio

---

## Current Open Source Work
- Contributing to Zephyr RTOS
- Improving Renesas RA8M1 board/sample support
- Exploring Cortex-M85 CMSIS-DSP and Helium acceleration paths

---

📫 mahad.faisal@gmail.com
