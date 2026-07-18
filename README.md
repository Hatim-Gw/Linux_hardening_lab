# Linux Hardening Lab

## Objective

A practical, hands-on lab hardening an Ubuntu Server 26.04 LTS box across five layers: SSH configuration, firewall rules, brute-force protection, user/password policy, and system logging. Each layer was tested from a Kali Linux attacker VM to confirm the control actually works, not just that it was configured.

The goal isn't just "apply settings from a guide" — each writeup documents what was done, how it was verified, and any problems hit along the way.

## Environment

- **Target:** Ubuntu Server 26.04 LTS
- **Attacker:** Kali Linux
- **Hypervisor:** VMware Fusion Professional 25H2u1
- **Network:** NAT

## Writeups

| # | Topic | What it covers |
|---|---|---|
| 1 | [SSH Hardening](writeups/1.ssh.md) | Custom port, disabled root login, backup/restore config, `ssh.socket` override issue |
| 2 | [UFW Firewall](writeups/3.ufw_Practical.md) | Default-deny policy, allow-listing only the SSH port, nmap verification (open vs. filtered) |
| 3 | [Fail2Ban](writeups/4.fail2ban.md) | SSH jail configuration, triggered lockout, verified ban, manual unban |
| 4 | [User Restrictions](writeups/5.user_rstrictions.md) | Root login disabled, sudo policy review, password complexity rules |
| 5 | [Logging](writeups/6.logging.md) | rsyslog live auth monitoring, auditd file-watch rule, persistence fix after reboot |

Each writeup follows the same structure: **Objective → Steps Performed → Problems Encountered**, so failures and fixes are documented alongside the working setup.

## Key Takeaways

- Every control was verified from the attacker side (Kali), not just confirmed in a config file on the target.
- Hardening builds in layers: firewall blocks unwanted traffic, Fail2Ban stops brute-forcing on what's left open, user/password policy limits what a valid login can do, and logging catches what slips through.
- Real problems came up at almost every stage (SSH socket override, port mismatches, audit rules not persisting across reboot) — each is documented as it was actually encountered, not smoothed over.
