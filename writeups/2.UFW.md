
# UFW
It is an abbreviation for Uncomplicated Firewall. It is used for filtering input and output packets to manage the traffic (allow/deny/reject/limit).

Moreover, **ufw** depends on **nftables**, which is the real tool in the Ubuntu kernel that deals with traffic, so whenever you write a command the ufw translates it nftables, then nftables executes the command.


- For hardening, **incoming packets to the server** should be denied by default.
- For **outgoing packets, we trust our server** so they should be allowed by default.


# actions

- allow

- deny (dropping the packets)

- reject (notify the sender that his packet is rejected)

- limit (limit the number of connection failures for each IP)



