# iOS Reverse Engineering Cheetsheet

## Mach-O files

### Header

### String Table

### Symbol Table

### Codesigning HashTable


## ARM64 Registers

### General Purpose

### Exception Registers:
***EL0: User-Mode***
***EL1: Kernel-Mode (XNU / iBoot)***
***EL2: Hypervisor, assumably not used on iOS***
***EL3: Secure Monitor (KPP / Watchtower) / (LLB runs here at boot)***


### Execution
***CPSR / SPSR: Processor State Register***
***FP: Frame Pointer***
***PC: Process counter***
***LR: Linking register, contains address of executed function***
***SP: Stack Pointer***

## ARM64 Instructions

## ARM64 System Instructions
