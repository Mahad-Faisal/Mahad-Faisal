<h1 align="center">Mahad Faisal</h1>

<h3 align="center">
Embedded Controls & Firmware Engineer | Real-Time Systems | Battery Intelligence | Power Electronics
</h3>

<p align="center">
Computer Engineering @ Drexel University · Graduating June 2027
</p>

I build real-time embedded systems that connect **hardware, firmware, physical models, estimation, and control**.

My work spans low-level MCU bring-up, RTOS architecture, motor-control platforms, battery-management systems, state estimation, model-based development, embedded AI, vehicle controls, and SIL/HIL validation.

I previously worked as an **Embedded Firmware Engineer Co-op at Rheem Manufacturing**, where I developed production-oriented inverter firmware and commercial HVAC control software on Renesas RX platforms.

---

## Current Focus

### Formula SAE Electric Vehicle — AMS, ECU & Vehicle Controls

Developing firmware across the Formula SAE EV accumulator-management and vehicle-control stack using **STM32F7 + FreeRTOS**.

Key work includes:

- Custom accumulator-management firmware interfacing with **ADBMS6830** battery-monitor ICs
- Pack voltage, temperature and current acquisition with freshness and coherency supervision
- PEC validation, usable-cell masks and stale-data rejection
- Debounced and latched battery safety faults
- Adaptive battery **SoC / SoH / thermal-state estimation**
- Multi-horizon **State-of-Power, DCL and CCL** calculation
- Battery-aware torque authority and fail-zero power limiting
- CAN communication between AMS, ECU, inverter and vehicle subsystems
- CAN bus-off recovery, heartbeat monitoring and protected message generations
- Current-model and residual-based diagnostics
- Thermal-management and coolant-control firmware
- SD-card telemetry and estimator diagnostic logging
- Deterministic host/SIL test infrastructure with fault injection
- GCC/Clang builds, ASan/UBSan and CI regression testing
- Scheduler and CAN-authority stress testing

The goal is not just to calculate battery state, but to safely propagate that information all the way into **real-time vehicle torque authority**.

---

## Embedded Battery Estimation & Edge AI Research

### Adaptive Electrothermal Battery State Estimation
**Renesas RA8M1 · Cortex-M85 · FreeRTOS · CAN · CMSIS-NN**

Designed and implemented a physics-first embedded battery-estimation platform combining an adaptive electrothermal estimator with bounded learned voltage-residual correction.

Core system:

- 5-state electrothermal **2RC equivalent-circuit model**
- Adaptive Extended Kalman Filter architecture
- Online battery resistance adaptation
- Adaptive measurement-noise estimation
- SoC, polarization-voltage and thermal-state estimation
- Deterministically bounded neural voltage-residual correction
- Explicit authority limiting so learned corrections cannot dominate estimator behavior
- Real-time CAN measurement interface
- Dual-MCU hardware-in-the-loop validation
- Cortex-M85 embedded deployment
- FP32 and INT8 inference experiments using Arm CMSIS tooling

Research validation includes:

- **4,500 Monte Carlo validation cases**
- zero estimator divergence in the evaluated campaign
- zero covariance failures
- zero learned-authority bound violations
- measured embedded execution timing and memory usage

A manuscript based on this work has been submitted to **IEEE Transactions on Transportation Electrification**:

> **Bounded Neural Voltage-Residual Correction for Embedded Battery State Estimation in Electrified Vehicles**

---

## Renesas + Zephyr RTOS

Contributing upstream-oriented Renesas support to **Zephyr RTOS**.

### Renesas RA GPT Counter Driver

Developed a hardware-validated Zephyr counter driver for the Renesas RA General PWM Timer.

Implemented:

- Zephyr counter-driver API integration
- Renesas FSP GPT backend
- Devicetree bindings
- Kconfig integration
- CMake integration
- counter start/stop/read functionality
- channel-alarm support
- interrupt and callback handling
- hardware validation on **EK-RA8M1**

During hardware bring-up, diagnosed a Renesas FSP event-path difference where timer alarms arrived through the capture/compare path rather than the initially expected compare event.

Also working with:

- Zephyr devicetree
- device-driver model
- Kconfig
- CAN / CAN-FD
- PWM
- ADC
- CMSIS-DSP
- Renesas RA8M1 / RA8P1 platforms

---

## Formula SAE Dashboard & DAQ

Developing a next-generation vehicle dashboard/DAQ platform using:

**Renesas RA8P1 + Zephyr + LVGL**

Architecture includes:

- canonical vehicle-state model
- freshness-aware CAN data
- acquisition → state → UI separation
- thread-safe telemetry handling
- LVGL dashboard rendering
- fault-injection CLI
- DAQ-oriented interfaces

Previously implemented the dashboard using FreeRTOS/FSP before migrating the platform to Zephyr.

---

## Professional Embedded Firmware Experience

### Embedded Firmware Engineer Co-op — Rheem Manufacturing
**January 2025 – September 2025**

### RX26T Three-Phase ACIM Inverter

Served as the primary firmware developer for a Renesas RX26T-based three-phase HVAC inverter platform.

Worked across:

- MCU clock and startup configuration
- pin multiplexing
- ADC acquisition
- PWM generation
- complementary outputs and deadtime
- POEG hardware protection
- linker and flash-memory configuration
- interrupts and timers
- PWM command measurement
- motor-speed feedback
- thermistor acquisition
- watchdog handling
- boot and fallback behavior

Ported and integrated Renesas motor-control software across MCU platforms and validated gate drive, current sensing, PWM behavior and protection paths on hardware.

### EMI / Reset Root-Cause Debugging

Investigated ignition-sparker-induced inverter resets using post-failure UART instrumentation and hardware testing.

Reduced reset occurrence from approximately:

**45% → 1.5% through firmware mitigation**

and ultimately to:

**0% after hardware filtering**

The investigation included interrupt behavior, ADC recovery, watchdog starvation and electrical-noise interaction with firmware execution.

### Commercial HVAC FreeRTOS Migration

Migrated a large Renesas RX66N commercial HVAC controller from a bare-metal superloop architecture to **FreeRTOS**.

Worked on:

- task decomposition
- scheduler design
- software timers
- semaphores
- message passing
- ISR/task interaction
- stack and heap sizing
- timing analysis
- UART resource contention
- electrical-load validation

The platform was being modernized to support future communications, connected-device and embedded-intelligence capabilities.

### Embedded Communications & Tooling

Also developed:

- proprietary HVAC communications over SCI/UART and RS485
- interrupt-driven communication interfaces
- reusable communication integration templates
- firmware parameter/bytestream generation tools
- CRC insertion
- endian conversion
- structured binary headers
- Excel ↔ firmware-data conversion
- Python-based engineering utilities

---

## Model-Based Development & Controls

Working with **MATLAB / Simulink** for embedded physical-system development.

Current areas include:

- electrothermal battery modeling
- equivalent-circuit parameterization
- HPPC-based characterization
- adaptive state estimation
- thermal observers
- SoP / DCL / CCL calculation
- Model-in-the-Loop validation
- Software-in-the-Loop testing
- Hardware-in-the-Loop testing
- Embedded Coder workflows
- generated-code integration with production C firmware

---

## Senior Design — Battery-Aware Grid-Forming Inverter

Beginning development of a Renesas-based three-phase grid-forming inverter platform combining real-time power-electronics control with battery-state estimation.

Planned architecture:

**Battery → Bidirectional DC/DC → 48 V DC Link → Three-Phase Inverter**

using:

- **RA8T2** for fast inverter / converter control
- **RA8M1** for battery estimation and higher-level energy management
- CAN-FD communication between control domains
- dq control and SVPWM
- grid-forming / virtual-synchronous-machine concepts
- battery State-of-Function constraints on inverter power dispatch

The goal is to connect battery electrochemical capability directly to real-time power-electronics control.

---

## Areas of Depth

### Embedded Firmware
- Bare-metal C
- FreeRTOS
- Zephyr RTOS
- interrupt-driven systems
- MCU bring-up
- memory / linker configuration
- watchdog and fault handling
- real-time scheduling

### Embedded Hardware Interfaces
- CAN / CAN-FD
- UART / RS485
- SPI
- I2C
- ADC
- PWM
- timers / capture
- GPIO
- hardware protection peripherals

### Controls & Physical Systems
- motor-control firmware
- inverter systems
- battery-management systems
- Kalman filtering
- electrothermal modeling
- State-of-Power estimation
- battery-aware vehicle control

### Verification
- MiL
- SiL
- HiL
- deterministic fault injection
- host-based embedded testing
- sanitizers
- CI/CD
- hardware bring-up and instrumentation

### Embedded AI
- physics + ML hybrid architectures
- bounded learned corrections
- Cortex-M85 deployment
- CMSIS-NN
- INT8 inference
- Arm Helium / MVE exploration

---

## Technologies

**Languages**

`C` `C++` `Python` `MATLAB`

**Embedded / RTOS**

`FreeRTOS` `Zephyr` `Renesas FSP` `STM32 HAL`

**MCUs**

`Renesas RX26T` `RX66N` `RA8M1` `RA8P1` `RA8T2` `STM32F767` `ESP32`

**Interfaces**

`CAN` `CAN-FD` `SPI` `I2C` `UART` `RS485` `ADC` `PWM`

**Development**

`Git` `CMake` `Ninja` `GCC` `Clang` `Jenkins` `Linux` `Renesas e² studio` `STM32CubeIDE`

**Modeling / Validation**

`MATLAB` `Simulink` `Embedded Coder` `SIL` `MIL` `HIL`

---

## What I Like Working On

I am particularly interested in engineering problems that cross traditional boundaries:

**physical system → sensors → MCU peripherals → RTOS → estimation → control → communications → system behavior**

I enjoy going deep into individual technical areas, but I am equally interested in understanding and engineering the interfaces between them.

Current interests include:

- embedded controls
- EV and battery systems
- power electronics
- safety-critical firmware
- real-time operating systems
- Renesas MCU platforms
- state estimation
- model-based development
- embedded AI
- firmware verification infrastructure

---

## Contact

**Email:** mahad.faisal@gmail.com
