

## 🔍 5. Testing & Verification

### 5.1 Ping Tests  
Did the PC successfully ping a DNS name (e.g., `library_pc1`)?  
Explain the result.

Yes, the PC successfully pinged the DNS names pc1 and pc2.

The DNS server translated pc1 into 192.168.2.100 and pc2 into 192.168.2.101. Both tests received 4 replies out of 4 packets sent, with 0% packet loss.

This confirms that DNS name resolution and network communication were working for these two hostnames.

The ping pc3 test failed because the DNS server could not find a record for that hostname.

<img width="687" height="577" alt="image" src="https://github.com/user-attachments/assets/f71df1e6-c1bc-4318-a50d-38b19ac80d91" />


---

### 5.2 DNS Resolution  
Describe whether DNS resolved the hostname correctly.

I tested DNS resolution using the ping command from PC0 in Cisco Packet Tracer.

When I entered ping pc1, the DNS server resolved the hostname to 192.168.2.100. When I entered ping pc2, it resolved the hostname to 192.168.2.101.

Both tests were successful, with four packets received and 0% packet loss.

This confirms that the DNS server correctly translates the configured hostnames into IP addresses, allowing computers to communicate using names instead of typing IP addresses manually.

---

### 5.3 DHCP Lease Verification  
Describe the IPs assigned to each PC.  
Do they match the DHCP pool?
I verified the DHCP configuration using the ipconfig /all command in Cisco Packet Tracer.

The three PCs successfully received their IP addresses automatically from the DHCP server.
PC0 --> 192.168.2.100 --> Successful
PC1 --> 192.168.2.102 --> Successful
PC2 --> 192.168.2.101 --> Successful

All three PCs received the subnet mask 255.255.255.0, default gateway 192.168.2.1, and DNS server 192.168.2.2.

This confirms that the DHCP server successfully distributes unique IP addresses and the required network settings to the client computers.

<img width="695" height="721" alt="image" src="https://github.com/user-attachments/assets/178f0146-2bca-4ee7-9eb0-3687ab3d0848" />


