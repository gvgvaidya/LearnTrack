
JVM basics

JDK vs JRE vs JVM
- JDK is the development kit. It includes tools like javac, the JVM, and libraries.
- JRE is the runtime environment. It includes the JVM and libraries needed to run Java programs. It does not include the compiler.
- JVM is the virtual machine that executes Java bytecode. It manages memory and uses JIT compilation to run on different platforms.

Bytecode
- bytecode is the intermediate .class output created by the compiler
- the JVM reads bytecode and executes it on the host machine

Write once, run anywhere
- Java source is compiled to bytecode
- any operating system with a compatible JVM can run that bytecode
- portability comes from the JVM abstracting away OS and hardware differences
