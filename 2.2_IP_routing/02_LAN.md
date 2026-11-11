
# 2. Part B — Configuring the LAN

## 2.1 Static IP Configuration
### Pi A (192.168.50.1)
<img width="683" height="92" alt="image" src="https://github.com/user-attachments/assets/1fd0a6be-f4e7-4a31-b6b9-61b7a0315c14" />


### Pi B (192.168.50.2)
The other team configured Pi B. We did not capture a screenshot of
Pi B's IP configuration. From Pi B, we pinged Pi A at 192.168.50.1
and received four replies with 0% packet loss. From Pi A, we also
pinged Pi B at 192.168.50.2 and received four replies with 0% packet loss.

<img width="678" height="190" alt="image" src="https://github.com/user-attachments/assets/87799579-5ac4-4697-a86c-21dbe4816145" />


## 2.2 Explanation
Explain:
- What is a static IP address?

A static IP address is an address we set manually on a device.
We used 192.168.50.1 for Pi A and 192.168.50.2 for Pi B.


- Why both devices cannot use the same address

Each Raspberry Pi needs a unique IP address on the LAN. If both
use the same address, an IP address conflict can make it unreliable
to reach the intended device.


- Why we use /24

We used /24, which is equivalent to the subnet mask 255.255.255.0.
The first 24 bits identify the network, and the last 8 bits identify
the host. Both addresses belong to the 192.168.50.0/24 subnet, so
the two Pis can communicate directly over Ethernet without a gateway.

