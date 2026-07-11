# Linxu_Hardening_lab

# Objective
learning Linux hardening on Ubuntu server version **26.04 LTS**

Due to the fact ssh service is widely used for managing Ubuntu servers, it has become a vulnerable threat for hackers to get easy access to servers, which means protection procedures are needed.

SSH hardening makes it more difficult for hackers to gain access to the system by changing the default values of ssh configuration files
- port number
- root permission
- password authentication
- ...

# Environment:
- Ubuntu server 26.04 LTS
- VMware Fusion Professional 25H2u1
- network protocol: NAT


# Steps:
1. checking SSH status using the command

**sudo systemctl status ssh**


<img width="1424" height="1106" alt="image" src="https://github.com/user-attachments/assets/78bced72-d976-47c5-8f73-6a1e173df404" />

3. Backup the configuration file and change the default values of port&permissions&athentications


**sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak**  (this command for the backup)

Then, edit the values in sshd_config
**sudo nano /etc/ssh/sshd_config**

<img width="1170" height="1288" alt="image" src="https://github.com/user-attachments/assets/c2ec2864-7f30-4dc8-9e74-25154797ee26" />


Afterward, change the configuration of ssh.socket (only for later versions of Ubuntu)


<img width="1016" height="726" alt="image" src="https://github.com/user-attachments/assets/0c6d296f-f9c5-49fd-95f2-aee7b758dfef" />

3. restart the ssh service and ssh.socket using


**sudo systemctl restart ssh ssh.socket**

<img width="1430" height="592" alt="image" src="https://github.com/user-attachments/assets/15c03423-82a5-4837-8ac8-da9499d57dee" />



# Problems Encountered

- once I edited the **ssh_config** file I restarted the service and it didn't work so I had to search the problem then I found in later versions of ubuntu ssh.socket needs manual change beside the ssh_config, If you change one of them alone the port wouldn't change
