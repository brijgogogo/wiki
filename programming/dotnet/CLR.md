= CLR =

Common Language Runtime (CLR) provides runtime features like automatic memory management, exception handling, etc.

CLR is language-neutral. C# is one of several `managed languages` that get compiled into managed code. Managed code is represented in `Intermediate Language` or IL. The CLR converts the IL into native code of the machine, such as X86 or X64, usually just prior to execution. This is referred to as Just-in-Time (`JIT`) compilation. Ahead-of-time compilation is also available to improve startup time.


The container for managed code is called an `assembly` or `portable executable`. An assembly can be an executable file (.exe) or a library (.dll), and contains not only IL, but type information (metadata). The presence of metadata allows assemblies to reference types in other assemblies without needing additional files.

A program can query its own metadata (`reflection`) and even generate new IL at runtime (`reflection.emit`).

Tools for IL:
* ildasm
* ILSpy
* dotPeek (JetBrains)
* Reflector (Red Gate)
