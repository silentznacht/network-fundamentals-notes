
### Models vs Protocols

**Simplified**
	- **Network models** (like OSI or TCP/IP) are **frameworks**. They tell us **what kind of tasks need to happen** at each layer of communication but don’t dictate exactly how. Think of them as “blueprints.”
	- **Protocols** are **rules and procedures** that actually implement these tasks. They define **how data is formatted, transmitted, secured, and interpreted**.

- **Models** are conceptual frameworks that organize how network communication works into layers.
    
    - Example: OSI Model (7 layers), TCP/IP Model (4 layers).
        
    - Purpose: provide structure and a common reference for designing, teaching, and troubleshooting networks.
        
- **Protocols** are the specific rules and standards used within those layers to perform tasks.
    
    - Example: HTTP (web), TCP (reliable delivery), IP (addressing), DNS (name resolution).
        
    - Purpose: define _how_ data is formatted, transmitted, received, and interpreted.
        
- **How they work together**:
    
    - The **model** acts like a blueprint, showing where each function belongs.
        
    - The **protocols** live inside the model’s layers and carry out the actual work of communication.
        
    - Different protocols are chosen depending on the occasion (e.g., HTTPS for secure web browsing, FTP for file transfer).


[[Protocols Types]]
[[Protocol Functions]]
[[Protocol Interaction]]