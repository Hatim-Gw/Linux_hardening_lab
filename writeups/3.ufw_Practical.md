
# commands
- ufw status verbose
- ufw status numbered
- ufw enable
- ufw allow [port number]/[tcp/udp]


# steps

1. enabled the ufw using **ufw enable**

<img width="726" height="164" alt="image" src="https://github.com/user-attachments/assets/dfdb1c9c-a5cf-4f2a-b237-dd28ea8f14a7" />

2. Afterwards, I allowed the specific port using **ufw allow 48222/tcp**
<img width="784" height="56" alt="image" src="https://github.com/user-attachments/assets/5e6afaac-a020-4eb9-8416-6971af11f145" />


3. then, I sat defaults for incoming and outgoing packets to deny and allow.
    - sudo ufw default deny incoming
    - sudo ufw default allow outgoing




4. Checked the status of the firewall using **ufw status verbose**

<img width="916" height="576" alt="image" src="https://github.com/user-attachments/assets/887a87ca-418a-4955-a6af-be3a8f61b023" />


5. inspect the port from the Kali using
    - nmap -p 22 [server_ip]
    - nmap -p 48222 [server ip]
      

    - <img width="1186" height="828" alt="image" src="https://github.com/user-attachments/assets/2eaa1bd9-d533-4aa1-a9ef-5ecab10b6546" />


6. connect remotely to ubuntu server using ssh
   - ssh -p 48222 [username]@[server_ip]
  -<img width="1288" height="536" alt="image" src="https://github.com/user-attachments/assets/edd78cc7-b2e2-400d-913d-9533712896bf" />


