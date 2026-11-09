network-lab
Labs, notes, and projects from my CCNA journey. Focus: Layer 1-2 networking.

## Week 1

### Day 1: Network Devices (Nov 8, 2026)

**What I learned**
- **End hosts** (PCs, servers, phones, etc.) are the devices that use the
  network.
- **Switches** connect end hosts inside a LAN.
- **Routers** connect a LAN to other networks. A LAN needs a router to reach
  the internet.
- **Firewalls** filter traffic and can be connected either inside or outside
  the LAN.

**Lab**
- Built two LANs in Packet Tracer:
  - **LAN 1:** 2 PCs, 1 switch, 1 firewall, and 1 router
  - **LAN 2:** 2 servers, 1 switch, 1 firewall, and 1 router
- Connected both LANs to the internet and to each other.
- Added an attacker laptop to the network.


### Day 2: Interfaces and Cables (Nov 9, 2026)

**What I learned**
- **Copper cables:** Straight-through cables connect different device types
  (e.g., PC to switch, switch to router). Crossover cables connect the
  same device types (e.g., switch to switch, router to router, PC to PC).
  Modern devices with Auto-MDIX detect the cable type automatically.
- **Fiber cables:**
  - Single-mode has a thinner core, uses a laser, and reaches much longer
    distances.
  - Multimode has a thicker core and is used for shorter distances (550 m).
  - Mixing the two types causes connection failures or heavy signal loss.

**Lab**
- Built a topology with 4 routers, 8 switches, 3 PCs, and 1 server in
  Packet Tracer and connected them with cables chosen by distance
  and device type.

<img width="1042" height="597" alt="day2-topology" src="https://github.com/user-attachments/assets/63561e76-2efb-4d28-bb4a-0922f7e3d3f7" />


**Cable choices**

| Link | Distance | Cable | Why |
|------|----------|-------|-----|
| R1-R2 | 50 m | Copper crossover | Router to router, within 100 m copper limit |
| R3-R4 | 250 m | Multimode fiber | Too long for copper, short enough for multimode |
| R1-R3 | 3 km | Single-mode fiber | Too long for multimode |
