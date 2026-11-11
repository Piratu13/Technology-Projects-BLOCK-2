
# 3. Part C — Connectivity Test (ping)

## 3.1 Pi A → Pi B

From Pi A, we ran `ping -c 4 192.168.50.2`. Pi B replied to all
four requests, with 0% packet loss.


<img width="725" height="184" alt="image" src="https://github.com/user-attachments/assets/84ab577d-ab44-4cbf-9f97-8f36290317b8" />


## 3.2 Pi B → Pi A

From Pi B, we pinged Pi A at `192.168.50.1`. Pi A replied to all
four requests, with 0% packet loss.

<img width="664" height="212" alt="image" src="https://github.com/user-attachments/assets/86ac7e89-718f-464e-9e73-c7565f2829f7" />


## 3.3 Interpretation
Explain what the ping results mean and what errors might look like.

The replies confirmed that both Raspberry Pis could reach each
other over the direct Ethernet connection. During setup, running
`ping` without a destination returned `Destination address required`.
A ping sent to a destination can also time out if no reply comes
back. In that case, we would check the Ethernet link and the IP
addresses on both devices.


