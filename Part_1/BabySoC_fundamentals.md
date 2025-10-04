# BabySoC Fundamentals
------------------------------
## SOC (System-On-Chip)
------------------------------
A System-on-Chip integrates all essential parts of a computing system—such as the processor, memory, communication interfaces, and peripheral devices—onto a single silicon die.
Instead of using multiple chips on a PCB, SoCs combine everything into one integrated circuit, which results in lower power consumption, smaller size, and faster performance.

SoCs are widely used in embedded systems, mobile devices, automotive electronics, and AI accelerators, where efficiency and compactness are key.

## Main Components of a Typical SoC
--------------------------
A standard SoC consists of the following hardware building blocks:

<b>Processor (CPU/Core)</b>
Executes software instructions and controls overall system behavior. Commonly implemented with architectures like RISC-V or ARM.

<b>Memory Units</b>
Include on-chip SRAM, ROM, and memory controllers that handle external DRAM or flash. These store both instructions and data required during program execution.

<b>Peripherals</b>
Provide communication and control interfaces such as UART, SPI, I²C, GPIOs, timers, and interrupt controllers. They allow the processor to interact with the outside world.

<b>Interconnect / Bus Fabric</b>
The communication backbone that connects the CPU, memory, and peripherals. Examples include AXI, AHB, or APB buses.
It manages data transfers, arbitration, and address decoding.

<b>Glue Logic and Support Blocks</b>
Components such as clock/reset generators, power gating circuits, and domain crossings ensure reliable system operation and integration.

<b>Hardware Accelerators (optional)</b>
Specialized blocks like cryptographic engines, DSPs, or AI cores designed for high-speed computation on specific workloads.

Each of these modules is carefully integrated so that data moves efficiently across the system while maintaining synchronization and power efficiency.
