# GmodRawinput2
GmodRawinput2 for 32 bit

Summary: Why GMod’s Raw Input Handling is Broken and Why RawInput2.exe Can’t Fix It
Garry’s Mod (GMod) has fundamentally flawed raw input handling, which makes it impossible to properly port RawInput2.exe. Unlike Counter-Strike: Source (CS:S), which processes raw input in sync with the game’s tick rate, GMod's raw input logic is desynchronized, inconsistent, and laggy by default.

Key Issues with GMod’s Raw Input Handling
✔ Raw input updates even when no movement is happening.
✔ Polling is inconsistent and desynchronized from the game’s tick rate.
✔ Movement input is applied at incorrect times, leading to stuttering and lag.
✔ Even without external modifications, GMod’s input is inherently sluggish.
✔ Input appears to be applied before physics updates, causing unnatural acceleration.

Why RawInput2.exe Can’t Fix This
🚫 RawInput2.exe relies on the game already handling raw input correctly.
🚫 Since GMod’s raw input is flawed at the base level, smoothing it externally won’t fix the issue.
🚫 Even if movement is spread evenly (like in CS:S), GMod still applies it incorrectly.
🚫 The only real fix requires modifying GMod’s internal input processing.

Conclusion
The core issue lies in GMod’s raw input pipeline, not in how RawInput2.exe processes movement. Until Facepunch fixes this at the engine level, raw input in GMod will remain unreliable, making a proper RawInput2.exe port functionally impossible.
