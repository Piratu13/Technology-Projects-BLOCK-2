
# 5. Final Reflection
Answer:
1. Difference between physical cable and IP addressing  
The Ethernet cable provides the physical connection between the two
Raspberry Pis. IP addresses identify the devices on the network. We
used a cable tester to check the wiring, then used ping in both
directions to confirm that the Pis could reach each other by IP.

2. What surprised you most  
I was surprised to learn that the wires had to go into the RJ45
connector in a specific order and how easily they could shift while
I was inserting them. I was also surprised to see the file arrive
on Pi B after transferring it from Pi A with SCP.

3. Confidence level  
I feel confident that I could connect to Pi B again and use SCP
to transfer a file. I would like to build on that by practising
how to create files and folders on Pi B through an SSH session.

4. How to expand the LAN  
I would connect both Raspberry Pis and any additional devices to an
Ethernet switch. I could keep the 192.168.50.0/24 subnet and give each
new device a unique address, such as 192.168.50.3. I would use ping
to check that the new device could reach the existing devices.

5. One thing you'd explore next
I would explore how a router connects two different subnets. In this
lab, the two Pis were on the same subnet and could communicate
directly. I would like to see what changes when the destination is
on a different network.


