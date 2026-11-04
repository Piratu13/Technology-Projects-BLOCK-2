
## 🛠️ 3. Server Configuration (DHCP + DNS)

### 3.1 Static IP Settings  
Describe how you configured the server's static IP.
### 3.1 Static IP Settings

I configured the server's IP address manually in Cisco Packet Tracer by opening **Server0 → Desktop → IP Configuration** and selecting **Static**.

I entered the IP address `192.168.2.2`, and the subnet mask `255.255.255.0` was filled in automatically. I also manually configured the default gateway as `192.168.2.1`.

Using a static IP address ensures that the server keeps the same address so other devices can reliably access its DHCP and DNS services.

<img width="687" height="582" alt="image" src="https://github.com/user-attachments/assets/605a080b-ace6-45c9-a71f-d36672506821" />


---

### 3.2 DHCP Configuration  
Describe the DHCP pool you created (gateway, DNS, start IP, etc).

I configured manually a DHCP pool called serverPool on Server0 using Cisco Packet Tracer.
The DHCP pool is configured to automatically assign IP addresses from 192.168.2.100 to 192.168.2.149.

This allows the three PCs to obtain their network settings automatically instead of manually configuring each computer.

<img width="684" height="582" alt="image" src="https://github.com/user-attachments/assets/d94d39ba-28e6-43ab-92f6-abe025cd4c69" />



---

### 3.3 DNS Configuration  
Explain how you enabled DNS and created name records.

I configured the DNS service on Server0 in Cisco Packet Tracer by opening Services → DNS and turning the DNS service On.

I created two DNS A records by entering the hostnames and their corresponding IP addresses:
pc1 --> 192.168.2.100
pc2 --> 192.168.2.101
DNS allows computers on the network to use hostnames instead of IP addresses, making communication easier for users.

<img width="688" height="581" alt="image" src="https://github.com/user-attachments/assets/f5eb09d7-cc98-42ff-a59c-f6299d861218" />


