# A Payload's Life

## Staged Payloads
- Something runs a payload stager
	- 1 *Allocate memory* in a process
	- 2 Copy payload stager to tha memory
	- 3 *Create thread* in process to run stager
- Payload stager downloads encoded payload
	- 4 Stager *allocates memory* from payload
	- 5 Stager downloads encoded payload
	- 6 Stager passes execution to encoded payload
- Encode payload decodes payload
	- 7 Encoded payload decodes Reflective DLL in-place
	- 8 Encoded payload passes execution to Reflective DLL blob
- Payload initializes and runs
	- 9 Reflective DLL *allocate memory*
	- 10 Reflective DLL initializes itself in new memory
	- 11 Reflective DLL calls payload entry point

## Stageless Payloads
- Something runs a payload stage
	- 1 *Allocate memory* in a process
	- 2 Copy payload stage to tha memory
	- 3 *Create thread* in process to run stage
- Payload initializes and runs
	- 4 Reflective DLL *allocate memory*
	- 5 Reflective DLL initializes itself in new memory
	- 6 Reflective DLL calls payload entry point


## Artifacts


## Process Injection


## Process Hollowing

