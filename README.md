# mtasa-black

netc.dll is responsible for handling network communication within MTA:SA.
Custom AES-256 encryption with a non-standard key derivation function was used for network communication.
Serial validation involved multiple stages, including checksum verification, cryptographic checks, and server-side validation.
The network protocol lacked robust error handling, contributing to the identified vulnerabilities.

FairplayKD.sys is a kernel-mode driver responsible for anti-cheat functionalities within MTA:SA. Its analysis proved significantly more challenging due to its kernel-level operation and aggressive anti-debugging techniques.
The driver's communication protocol contained a race condition vulnerability exploited by SerialEngine to bypass authentication. The driver utilizes kernel-level hooks to monitor system calls and processes.
It employs a variety of anti-cheat methods, including checks for memory modifications, injection attempts, and unusual network activity.

They are closed source, so I decided to have fun. Files will be attached when I feel they're ready. (Disassembly, decompilation + more tinkering results)
