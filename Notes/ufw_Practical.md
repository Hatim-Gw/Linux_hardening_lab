
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
