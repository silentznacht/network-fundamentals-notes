
An Ethernet switch may use a buffering technique to store frames before forwarding them. Buffering may also be used when the destination port is busy because of congestion. The switch stores the frame until it can be transmitted.![[Screenshot 2025-09-19 at 19-12-35 Cisco Networking Academy NETWORK FUNDAMENTALS (CET1600C - Fall 2025).png]]

### **Why buffering even matters**

When a switch receives Ethernet frames, it sometimes can’t forward them instantly — maybe because the destination port is busy, or traffic is coming in faster than it can go out. Instead of dropping packets right away, the switch **buffers** them in memory until it can send them out.

That’s what _switch memory buffering_ is all about: how the switch stores frames temporarily to handle congestion.

**Port-based (a.k.a. dedicated buffering)**
    - Each port gets its own little slice of buffer memory.
    - If frames pile up on port 1, only _that port’s_ dedicated memory can be used. It doesn’t borrow space from other ports.
    - **Pros**: Simple, predictable, no fighting over a shared pool.
    - **Cons**: If port 1 is slammed with traffic and its buffer is full, frames will be dropped — even if port 2’s buffer is sitting half empty. It’s not flexible.

**Shared memory buffering**
- Instead of carving up memory per port, all ports share a big pool of buffer memory.
- When any port needs to hold frames, it just grabs space from the shared pool.
- **Pros**: Much more efficient — traffic bursts on one port can borrow more buffer space as long as the pool has room. Better for uneven traffic.
- **Cons**: More complex logic, and if one port goes wild, it can hog the pool and starve other ports.