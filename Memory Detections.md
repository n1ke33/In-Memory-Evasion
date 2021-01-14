# Memory Detections

##  Memory Detections

- Use process, memory, and thread indicators to detect memory injected DLLs.  

- Install Process Hacker

 ## Proces, Thread, and Memory Properties

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

## Detections
 
 - Thread Start Address
     
     - No module associated with the start address.
     
     - DLLs are memory-mapped files. Injected DLLs aren't.
 
 - Memory Permissions
     
     - RWX permissions
     
     - Common pattern in offense tools
     
     - Odd AllocationProtect, Protect Pairs.
 
 - Memory Content
     
     - Signs of a PE file.
     
     - https://upload.wikimedia.org/wikipedia/commons/1/1b/Portable_Executable_32_bit_Structure_in_SVG_fixed.svg 
     
     - Strings associated with toolset.
    
## Memory Detection Applications
- Point-in-time Analysis

- "Hunt Assessment"

- Non-persisent software

- *Walk process*, threads, memory one-time

- Investigate content AND properties

- Report signs of malicious activity to analyst

- *Analyst reviews and determines actions*

- Some false postivies are OK
        
- Real-time Detection & Prevention

- Persistent software

- *Event driven*: new process, threads, more

- Investigate content AND properties

- Correlate multiple signs of malicious activity

- *Do nothing, fire alert, or deny action*

- Bias against false positives.

## Detection Tools

- Reflection Injection Detection
      
      - https://github.com/papadp/reflective-injection-detection
      
      - MZ header
      
      - RWX memory
      
      - Memory not associated with module

 
 - Get-InjectedThread.ps1 by Jared Atkinson
      
      - https://gist.github.com/jaredcatkinson
      
      - Thread StartAddress not associated with module
 
 
 - LOKI from Nextrin Systems
      
      - https://www.nextron-systems.com/
      
      - Scan file for YARA signature matches
        
 
 - YARA Rules from Loki and SPARK Scanners
      
      - https://github.com/Neo23x0/signature-base
      
      - Collection of YARA rules
 
