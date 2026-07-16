
# Objective:
After the setup of ssh, and UFW was finished, I started  implementing the fail2ban tool on the server to protect services from various threats such as brute-force attacks.

# commands
- sudo apt install fail2ban -y
- sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local
- sudo systemctl restart fail2ban
- sudo systemctl status fail2ban
- sudo fail2ban-client status sshd
- sudo fail2ban-client set sshd unbanip [Kali_ip]


# Steps performed:

1- I installed the fail2ban tool on the server using 
  - sudo apt install fail2ban -y

2- after investigating *jail.conf* It turns out I shouldn't modify it because it will be overwritten, so I copied it to local as documents recommend using
  - sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local
  - then I changed the command for *sshd* as shown in the next picture

  - <img width="1326" height="514" alt="image" src="https://github.com/user-attachments/assets/e29106ae-553c-4f9b-9402-9f4f5a283d5e" />

3- afterwards, I restarted fail2ban and checked its status using 
  - sudo systemctl restart fail2ban
  - sudo systemctl status fail2ban

  - <img width="1290" height="480" alt="image" src="https://github.com/user-attachments/assets/1ebb34a0-f1db-4b44-aaab-53c7a3597e5e" />


4- I attempted 3 logins using Kali to the Ubuntu server, which led to banning Kali's IP

  <img width="722" height="322" alt="image" src="https://github.com/user-attachments/assets/0d7ee79a-0b5a-414d-8839-cb78d8b52bea" />

5- I reviewed the status of fail2ban to see if the IP is banned or not using 
  - sudo fail2ban-client status sshd

  - <img width="936" height="388" alt="image" src="https://github.com/user-attachments/assets/665262c5-3ade-4be7-8763-3d4887b7d0ca" />

6- removed [kali ip] from fail2ban jail using
  - sudo fail2ban-client set sshd unbanip [Kali_ip]







