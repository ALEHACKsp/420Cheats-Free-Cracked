# 420Cheats-Free-Cracked

Did this because I was bored and didn't want to pay the ~$5 to crack the paid version. Peering into the cheat binary, you may notice several ReadProcessMemory calls... Why is this you ask? Because for some fucking reason this shit is external! Their loader injects this binary to GameOverlayUI.exe, for anyone wanting to play with this.

The loader hooks ntdll.dll!NtProtectVirtualMemory + ntdll.dll!ZwProtectVirtualMemory, and seems to protect against native injection. 

Peering into the function C420CheatsLoader::GiveDebugPrivileges(), you can see they deploy this tactic from https://anti-debug.checkpoint.com/techniques/interactive.html#self-debugging.

Included:               
.idb of free cheat loader (fixed imports using VMPImportFixer)                       
.dll of free cheat        (inject to GameOverlayUI.exe)

EDIT:
Added DarkAim DLL, their loader is the same. (Along with probably 10 other p2c's...)
