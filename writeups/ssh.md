# SSH
It's an abbreviation of Secure Shell, and it's been used to connect client hosts to Ubuntu servers to administer the servers remotely.
The privilege of using it instead of the old **telnet** is because of the encryption process between the server and the client.

# Availability of SSH

- By using the command ** systemctl status ssh
- <img width="1350" height="616" alt="image" src="https://github.com/user-attachments/assets/901e166a-6e88-421a-9e99-0a0fe57450bf" />
In the previous image it the **active(running)** means the service is working on the server. If it's not, we can change it with the command **sudo systemctl start ssh**.

-Moreover, to know the specific port ssh.socket is using, we can use the command **ss -tlnp**

# SSH configuration file
it's located in **/etc/ssh/sshd_config**

# ssh default port number
- ssh.socket listen on port **22** as default port, and listens to any ip address (0.0.0.0)


