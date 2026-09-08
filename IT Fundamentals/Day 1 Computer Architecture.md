
# First: what is a computer?

**Hardware** is the physical machine.
**Software** is instructions/data that tell the hardware what to do.
But there's an important middle layer:
> **The operating system manages hardware and provides services to applications.**
# CPU = **Central Processing Unit**.
Don't think of it simply as "the brain." That's too vague.
A CPU fundamentally:
> **fetches instructions, decodes them, and executes them.**
# CPU cores
A modern CPU can contain multiple **cores**.
Think of a core as an independent execution engine within the CPU.
For example:
```
CPU
├── Core 0
├── Core 1
├── Core 2
└── Core 3
```
A 4-core CPU can execute work on multiple cores simultaneously.
The operating system schedules **threads** onto CPU cores.
# Threads
A **thread** is an execution path within a process.
Example:
```
Application
    │
    └── Process
         ├── Thread 1
         ├── Thread 2
         └── Thread 3
```
The OS scheduler decides which threads get CPU time.
This is why your computer can appear to do hundreds of things simultaneously even though you don't have hundreds of CPU cores.
The CPU rapidly switches between work.
This is called **context switching**.
# CPU cache
This is where things get interesting.
The CPU is **extremely fast** compared with RAM.
If the CPU constantly had to wait for RAM, performance would suck.
So CPUs have small, very fast caches.
# RAM
RAM = **Random Access Memory**.
This is your computer's working memory.
Suppose you launch Firefox.
The executable and required data are stored on your SSD.
The CPU works primarily with data/instructions brought into its accessible memory hierarchy.
RAM is **volatile**.
Meaning:
> Power disappears → RAM contents disappear.
# Storage
Storage is where data persists.
Examples:
- HDD
- SATA SSD
- NVMe SSD
Your operating system lives there.
# Motherboard
The motherboard connects the major components.
Very simplified:
```
                 CPU
                  │
       ┌──────────┼──────────┐
       │          │          │
      RAM       PCIe       Chipset
                  │
             ┌────┴────┐
             │         │
           GPU        NVMe
```
It provides electrical connections and communication pathways between components.
# Buses / interconnects
Components need to communicate.
```
CPU ←→ RAM
CPU ←→ PCIe devices
CPU ←→ storage
CPU ←→ chipset
```
Modern systems use several interconnect technologies rather than one giant "bus."
You don't need to memorize motherboard electrical architecture yet.
The important sysadmin concept is:
> **Hardware components communicate through defined interfaces/interconnects.**
# NIC — Network Interface Controller
Your NIC allows the machine to communicate over a network.
It can be:
- Ethernet
- Wi-Fi
# Firmware
Here's an important distinction.
**Firmware** is software stored on/for hardware that provides low-level control and initialization.
Examples:
- Motherboard firmware
- SSD firmware
- NIC firmware
- GPU firmware
Your motherboard's firmware is what we commonly interact with as: **UEFI**
# BIOS vs UEFI
You'll hear people say:
> "BIOS"
even on modern machines.
Technically, most modern PCs use **UEFI**, not legacy BIOS.
### Legacy BIOS
Older firmware architecture.
### UEFI
Modern firmware environment.
UEFI can:
- Initialize hardware
- Configure hardware
- Locate bootloaders
- Provide boot services
- Manage boot entries
- Provide firmware configuration
So when your computer starts:
**Windows isn't running yet.**
The firmware is running first.


# Practical Learning

## Windows:
- Task Manger
	- Performance
- Device Manger
	- Network adapters
	- Storage controllers
	- Display adapters
	- Processors
- System Information Command `msinfo32`
	- BIOS Mode
	- Processor
	- Installed Physical Memory
	- Base Board
	- Boot Device
## Linux:
Commands;
`lscpu`
`free -h`
`lsblk`
`lspci`
`ip link`
