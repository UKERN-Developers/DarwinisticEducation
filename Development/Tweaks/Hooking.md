# Hooking
Hooking is programmatically changing the behaviour of a function call or module.

Hooking can be used for debugging, reverse engineering or exploitation purposes.

Despite hooking being mainly known from CydiaSubstrate on jailbroken devices it is possible to hook in sandboxed container apps as well.

## Dynamic Loading
Upon launch of a binary the dynamic loader loads libraries that are linked with it.

On iOS binaries use the Mach-O format and in the header of the binary information can be found about what libraries it is linked to.

iOS does require codesignatures and changing / patching the dynamic library load commands in the binary requires you to resign the binary.

When patching a dynamic library load command it is possible to make the dynamic loader load a different library upon launch of the binary, making it possible to replace function calls with your own logic, thus hooking.

Another method is to replace the actual dynamic library that the binary is loading, but this also requires the new dynamic library to be signed.

This method of hooking is mainly used when you do not have the source code of the program you are trying to hook.

If you have the sourcecode it would be better to use interpositioning.

Dynamic Loading Hooks are known from CydiaSubstrate, Theos Jailed and IPA Patch. They are possible with sandboxed container apps as well.


## Interpositioning

Interpositioning is programmatically replacing symbol calls in the \_\_DATA segment.

Interpositioning is quite easy to set up and therefore when having the source code of a program the most effective and fastest way to hook.

Interpositioning will replace all symbol calls with a symbol you have defined.

In your symbol (function) you can for example print out that a call to the function had been made, then call the original symbol and return.

This way your program gets an extremely high verbosity which is awesome when writing complicated logic.


## Receivers, Handlers, Callback and Mach

Mach Traps and Exception handlers, Thread State analysis and Event listeners can be used to debug an application with extreme verbosity.

These functions give the ability to get the state of the processor registers or listen for specific events to occur which is also quite nice when debugging a program.


## Introspection

Introspection is what we call monitoring the entire runtime of a process.

Live introspection means that all calls and all state information is monitored while it is happening.

What can be monitored is for example the stack memory changes, heap allocations / deallocations, processor states and usage, memory usage, disk write operations, network communications and packets, function calls etctera.

Introspection on kernel level is extremely useful when researching the kernel, but it requires a jailbreak and often a lot of more work to get kernel debugging to actually function.

Ian Beer will soon publish a new writeup on how to get kernel debugging to work for the Electra Jailbreak.


## IPA Patch

IPA Patch is a framework placeholder for patching / hooking apps from inside the sandbox.

Any appstore app that is decrypted can be used, like for example Whatsapp.

You can add your own code that is executed upon launch of the first responder and then it.


## Theos

Theos is injecting libraries into apps on jailbroken systems and provides a full development kit for hooking.

It is the best known hooking framework but sadly it's loading is a bit late which is in some occasions causing the hooks to fail.


## Theos Jailed

Theos jailed is an awesome way of hooking.

It is like theos with the same sdk but for non-jailbroken devices.

It randomly replaces a library load call with it's own library making hooking possible, though this again may come with the same issue as mentioned above.
