## RawInput2

An external software that ports [momentum mod's](https://momentum-mod.org/) ``m_rawinput 2`` behaviour. This option provides mouse interpolation which will ["line up with the tickrate properly without needing to have a specific framerate"](https://discord.com/channels/235111289435717633/356398721790902274/997026787995435088) (rio). The code for this isn't public and was reverse engineered from the game.

### Usage
* Launch the game in ``-insecure`` mode. (It wont work otherwise!)
* Run the application.
* Make sure to set ``m_rawinput 2`` in game for it to take effect.

### Building requirements
* [Microsoft Detours](https://github.com/microsoft/Detours)


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
