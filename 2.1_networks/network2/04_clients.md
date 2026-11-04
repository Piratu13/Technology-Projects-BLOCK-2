
## 💻 4. PC Configuration (DHCP Clients)

### 4.1 Explanation  
Describe how you configured PCs to obtain addresses automatically.
I configured the three PCs (PC0, PC1, and PC2) to obtain their IP addresses automatically using DHCP.

To do this, I opened each PC in Cisco Packet Tracer, navigated to Desktop → IP Configuration, and selected DHCP instead of Static.

The PCs successfully contacted the DHCP server at 192.168.2.2 and received their network settings automatically.

The DHCP server was configured to assign IP addresses starting from 192.168.2.100, with the subnet mask 255.255.255.0, default gateway 192.168.2.1, and DNS server 192.168.2.2.

This demonstrated how DHCP simplifies network configuration by removing the need to assign IP addresses manually to each PC.

### 4.2 Evidence  
📸 Screenshots of:
- PC IP Configuration (showing DHCP enabled)
<img width="847" height="267" alt="image" src="https://github.com/user-attachments/assets/f68fcb0e-5a13-404e-a871-188b21c77554" />

<img width="691" height="721" alt="image" src="https://github.com/user-attachments/assets/3e61a34d-d0a4-4dd8-b660-cac715c022d6" />

