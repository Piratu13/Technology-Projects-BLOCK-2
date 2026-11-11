
# 4. Part D — Practical LAN Application
Choose **one**:
- SCP file transfer  
- Shared SSHFS folder  
- Python chat program  

We used SCP to copy `testfile23.txt` from Pi A to Pi B 

## 4.1 Explanation
Explain what you did, issues encountered, and how you solved them.

We used SCP (Secure Copy) to transfer `testfile23.txt` from Raspberry
Pi A to Raspberry Pi B at `192.168.50.2`. An earlier attempt returned
`Permission denied`. We retried, authenticated successfully, and
confirmed that the transfer of `testfile23.txt` reached 100%.

On Pi B, some attempts to open the file returned `No such file or
directory` because we used the wrong filename. We then ran
`cat ~/testfile23.txt` and saw `Hello from raspberry pi A`. This
confirmed that the file arrived on Pi B and that we could read it.

<img width="673" height="354" alt="image" src="https://github.com/user-attachments/assets/78c58109-9fe8-45c3-91f1-a9798d717cd8" />


<img width="675" height="57" alt="image" src="https://github.com/user-attachments/assets/e3b4a5f5-f77e-4185-88db-38820f691710" />


