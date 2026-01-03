# 4. Physical Security

Physical security involves the use of controls to protect physical assets, personnel, and infrastructure from physical threats such as theft, vandalism, or unauthorized access. It is the foundation of information security—if an attacker can physically access a server, all logical and technical controls can be bypassed.

## Key Concepts

- **Layered Security (Defense in Depth)**: The fundamental principle of physical security. It involves creating multiple layers of defense, like the layers of an onion. An attacker must breach each layer in sequence to reach the protected asset. For a data center, this might look like: **Perimeter (Fence) -> Grounds (Lighting/Cameras) -> Building (Locks/Guards) -> Room (Access Control) -> Rack (Locked Cabinet)**.
    

## Perimeter and Grounds Security

- **Fencing**: The first line of defense, designed to define the property boundary and deter casual trespassers. Fence height and material are key deterrent factors.
    
- **Gates**: Controlled entry points in a fence. They should be as secure as the fence itself and monitored.
    
- **Bollards**: Short, sturdy posts used to prevent vehicles from ramming into buildings or accessing pedestrian areas. They are a critical anti-vehicle defense.
    
- **Lighting**: A powerful deterrent that eliminates hiding spots and improves the effectiveness of surveillance cameras and security guards.
    
- **Surveillance Systems (CCTV)**:
    
    - **Purpose**: Can act as a deterrent (visible cameras) and a detective control (recording events for investigation).
        
    - **Considerations**: Camera placement, resolution, field of view, and performance in low-light conditions are critical for effectiveness.
        

## Building and Room Access Control

- **Locks**: A basic preventative control. Can range from simple key-and-tumbler locks to more complex electronic locks and cipher locks that require a code.
    
- **Access Control Vestibule / Mantrap**: A highly effective entry control system consisting of two interlocking doors. The first door must close and lock before the second door can be opened. This prevents **tailgating** by forcing individuals to authenticate one at a time.
    
- **Tailgating vs. Piggybacking**:
    
    - **Tailgating**: An unauthorized person follows an authorized person through a secured entry point _without their consent_.
        
    - **Piggybacking**: An authorized person _knowingly_ allows an unauthorized person to gain entry (e.g., by holding the door open). This is often a result of social engineering.
        
- **Access Control Technologies**:
    
    - **Proximity Cards / RFID / NFC**: Contactless cards that are read by a card reader to grant access.
        
    - **Biometrics**: Using unique human characteristics (fingerprint, iris) for authentication at secure entry points.
        

## Environmental Controls

Protecting IT infrastructure from environmental threats is a key part of physical security.

- **HVAC (Heating, Ventilation, and Air Conditioning)**: Maintains a stable temperature and humidity within a data center to prevent servers from overheating or being damaged by static electricity.
    
- **Fire Suppression**:
    
    - **Detection**: Smoke detectors, heat detectors.
        
    - **Suppression Systems**:
        
        - **Water-based (sprinklers)**: Can be damaging to electronic equipment.
            
        - **Gas-based (clean agent)**: Displaces oxygen or chemically interrupts the fire, causing less damage to electronics but posing a risk to human life.
            
- **Power Management**:
    
    - **UPS (Uninterruptible Power Supply)**: Provides temporary battery backup power in the event of a brief power outage, allowing systems to shut down gracefully.
        
    - **Backup Generator**: Provides long-term power during extended outages.