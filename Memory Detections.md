# Memory Detections

##  Memory Detections
  - Use process, memory, and thread indicators to detect memory injected DLLs.
  
  - Install Process Hacker
  
  - Process Properties
    - Parent Process
    - Process Name
    - Process Signer
      - Don't risk to have false positivies with signs like "Microsoft"
      - They can get a free pass
    - Siganture Valid?
    - Command Line Arguments
    - Current Working Directory
    
  - Thread Properties
    - Thread ID
    - Start Address
    - Start Address Module
    - Priority
    
  - Memory properties
    - Base Address
    - Type of Memory
    - State of Memory
    - Size
    - File
    - Initial Permissions
    - Permissions
    
  - Detections
    - Thread Start Address
      - No module associated with the start address.
      - DLLs are memory-mapped files. Injected DLLs aren't.
    - Memory Permissions
      - RWX permissions
      - Common pattern in offense tools
      - Odd AllocationProtect, Protect Pairs.
    - Memory Content
    
## 

##

##
 
