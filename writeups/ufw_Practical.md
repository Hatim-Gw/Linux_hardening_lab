
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

then


3. Checked the status of the firewall using **ufw status verbose**

<img width="868" height="368" alt="image" src="https://github.com/user-attachments/assets/6bbd06e5-4146-4bdd-8209-bd07e6d75487" />

4. inspect the port from the Kali using
    - nmap -p 48222 [server ip]
  

    - <img width="1306" height="402" alt="image" src="https://github.com/user-attachments/assets/579a5054-303f-4ce7-b830-baa053bc2151" />

5. connect remotely to ubuntu server using ssh
  -<img width="1288" height="536" alt="image" src="https://github.com/user-attachments/assets/edd78cc7-b2e2-400d-913d-9533712896bf" />


