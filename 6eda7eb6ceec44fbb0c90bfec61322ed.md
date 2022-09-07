0. Configure DNS

Make sure DNS is configured so you have all the domain name and computer names

## 1st Method: Systemd resolve service

vi /etc/systemd/resolved.conf

> \[Resolve\]
> 
> DNS=

systemctl restart systemd-resolved

nslookup thmdc.za.tryhackme.com

## APPARENTLY THIS IS THE ONLY METHOD THAT WORKS. IT OVERRIDES THE OTHERS

## 2nd Method: edit /etc/resolv.conf

nameserver &lt;IP of DNS&gt;

domain &lt;Domain name of local host&gt;

search &lt;which domains to search, e.g. example.com&gt;

DO NOT RESTART SERVICE. If restarted, have to re-key in the details

sudo systemctl restart NetworkManager

**ALTERNATIVELY, USE GUI "Network Manager"**

- **Advanced Network Configuration -> Your Connection -> IPv4 Settings**
- **Set your DNS IP here to the IP for the DC in the network**
- **Add another DNS such as 1.1.1.1 or similar to ensure you still have internet access (optional)**
- **Run `sudo systemctl restart NetworkManager` and test your DNS.**

## **Test your DNS**

nslookup &lt;dc computername&gt;

id: 6eda7eb6ceec44fbb0c90bfec61322ed
parent_id: 0c2846bd3b824b53bfc522d03d0bb20b
created_time: 2022-07-12T07:55:18.305Z
updated_time: 2022-07-19T09:12:04.546Z
is_conflict: 0
latitude: 0.00000000
longitude: 0.00000000
altitude: 0.0000
author: 
source_url: 
is_todo: 0
todo_due: 0
todo_completed: 0
source: joplin-desktop
source_application: net.cozic.joplin-desktop
application_data: 
order: 1657618384300
user_created_time: 2022-07-12T07:55:18.305Z
user_updated_time: 2022-07-19T09:12:04.546Z
encryption_cipher_text: 
encryption_applied: 0
markup_language: 1
is_shared: 0
share_id: 
conflict_original_id: 
master_key_id: 
type_: 1