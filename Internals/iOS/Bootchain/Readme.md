# Bootchain

## SecureROM
The secure Read-Only Memory is what is reffered to as BootROM.  
The code on the SecureROM is flashed at production and can not be modified as the name already clarifies, it is read-only.  
Flaws in the algorithmic logic of the BootROM are persistant and can not be patched unless the device is taken into a factory and the chip is replaced.  
Apple Inc. can decide to make it harder to exploit flaws at SecureROM level but they can never fully prevent exploitation.  
Therefore jailbreaks built on BootROM level vulnerabilities are the most consistant.  
Internal references to BootROM can be found in the leaked source code of iBoot which may aid research on this absolute lowest-level of the iPhone software.  
Usually bugs can be found through analyzing dumps of BootROM.  
SecureROM code is loaded into the memory at a very early stage of the boot process, therefore when having code execution in the bootloader one can dump this code from the physical fixed memory address it is mapped to.  
With this dump one can create a section in IDA and combine it with a RAM and NOR dump taken from the same stage.  
Then vulnerabilities can be found and sometimes even implementations from Apple Inc. that are open-source can be used to symbolicate structures (e.g. Apple's memcpy).  
For symbolicating one would simply need to compile that source code from Apple Inc. and create a FLAIR import for the IDA.  
IDA will do the rest. 

## Low-Level Bootloader

## iBoot Single Stage

## iBoot Epoch Change

## iBoot 

## DeviceTree

## Secure BootChain

### SHSH Tickets (ApTicket)

## KernelCache

## RamDisk

## FileSystem
