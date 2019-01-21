# Dualboot / Multiboot

## What is a dual-boot
Dualboot means that you can install a multiple of Operating Systems on the device.  
This is a great asset in researching multiple Apple Operating System Builds on the same device.  
Apple has a strict policy preventing downgrading or changes to components of the secure bootchain.  
However, thanks to a convenient invention of a researcher called kloader one can put a jailbroken kernel in state in which it can be used to rebootstrap a patched boot-chain.  
This enables users to install multiple Operating Systems on one devices by creating additional filesystem partitions next to the original Operating System and kload the required bootchain components to boot the additional operating system(s).  

## Dualbooting with WayOut
WayOut is an application created by iOS Bootchain researcher Nyansatan (https://nyansatan.github.io).  
The skeuomorphistic mastermind created this app for making dualbooting to lower iOS versions easy for all users.  
The applications guides you to simple steps for installing additional Operating System builds and can get the build of your choice to be booted.  
Apart from this application, Nyansatan also released very detailed writeups on how this works and other great ones about bootchain patches.  


## Dualbooting with CoolBooter
Coolbooter is an application like WayOut build upon kloader that does very much the same as WayOut.  
This application is the work of Coolstar (@coolstarorg), a well-known researcher in the field of Apple Inc. their systems.  
What makes this a great tool is the amazing support Coolstar adds for the versions you can install and also the ability to choose system and data partition sizes.  



## Dualbooting manually
