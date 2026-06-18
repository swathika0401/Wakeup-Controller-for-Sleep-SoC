# Wakeup-Controller-for-Sleep-SoC
A low-power digital design project implementing a Wake-Up Controller for System-on-Chip (SoC) architectures. The controller monitors wake-up sources during sleep mode and restores system operation through PMU-controlled power management.
## Overview
The Wake-Up Controller is a dedicated hardware module designed to reduce power consumption in SoC-based systems. When the SoC enters sleep mode, most functional blocks are powered down while the Wake-Up Controller remains active in an Always-On (AON) domain.
The controller continuously monitors multiple wake-up sources and initiates the wake-up sequence whenever a valid event is detected. It communicates with the Power Management Unit (PMU) to restore clocks, power domains, and CPU operation.
## Objectives
- Minimize power consumption during idle periods.
- Support multiple wake-up sources.
- Enable reliable and fast wake-up operation.
- Improve energy efficiency in battery-powered systems.
- Provide seamless interaction with the PMU.
### Wake-Up Sources
- GPIO Interrupts
- RTC Alarm
- Timer Events
- Watchdog Timer
- External Interrupts
## Working Principle
1. The SoC operates in Active Mode.
2. When inactivity is detected, the PMU places the system into Sleep Mode.
3. The Wake-Up Controller remains active in the Always-On domain.
4. It continuously monitors configured wake-up sources.
5. Upon detecting a valid wake-up event:
   - Generates a wake-up request.
   - Communicates with the PMU.
   - Restores clocks and power domains.
   - Sends an interrupt signal to the CPU.
6. The CPU resumes normal execution.
## FSM States
- Active
- Sleep Request
- Sleep Mode
- Wake Detection
- Wake-Up Sequence
- Active
## Features
- Low-power operation
- Always-On monitoring
- Multiple wake-up source support
- PMU integration
- FSM-based control logic
- Fast wake-up response
- Scalable architecture
## Applications
- Internet of Things (IoT) Devices
- Wearable Electronics
- Automotive Electronics
- Smart Sensors
- Embedded Systems
- Battery-Powered Devices
- Edge Computing Systems

## Tools Used
- Verilog HDL
- EDA Playground
- Vivado / ModelSim
- GitHub

## Online Simulation

The complete design and simulation can be accessed through EDA Playground:

🔗 [View and Run Simulation](https://edaplayground.com/x/aEpK)

## Future Enhancements
- Multi-power-domain support
- Wake-up source prioritization
- Advanced power gating techniques
- Event logging and diagnostics
- Dynamic power management algorithms


## Author

**VM Swathika**  


---

## License

This project is intended for educational and research purposes.
