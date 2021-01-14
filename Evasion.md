# Evasion

## Evasions
- Thread Start Address
	- Current Process?
	- Do not call CreateThread with arbitrary pointer.
	- Remote Process?
	- Hijack existing thread with SetThreadContext, or LoadLibrary with CreateRemoteThread.
- Memory Permissions
	- Avoid RWX, RWX permissions
	- Map page permissions to something plausible
	- Map a DLL and overwrite its memory
- Memory Context
	- Don't look like a DLL (unless a DLL is expected)
	- Obfuscate/remove strings analysts may use
	- Obfuscate memory when not in use

## Process Context
- NOt all trees are treated equally
- Things that buy your process credibility:
	- Valid digital signature from a trusted entity
	- A plausible/safe parent process
	- A process not normally seen in offense activity

