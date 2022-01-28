Nmap Port Scan

For full initial scan by Ippsec:

> sudo nmap -sC -sV -oA nmap/initial &lt;ip or cidr&gt;

Simple initial scan with OS detection >--top-ports only scan the N most common ports

> sudo nmap -sV -O --top-ports 50 --open -oA nmap/simpleinitial &lt;ip or cidr&gt;

sudo nmap -sC -sV -O --open -p- -oA nmap/full &lt;ip or cidr&gt;

UDP Scan - Will take a very long time -- last resort

> sudo nmap -sU -p- -oA nmap/udp <ip or cidr

id: ccf82d46fdfe450db638dbb1fefc196c
parent_id: 6b8d3e46660447279f5aee899ce00b64
created_time: 2022-01-14T02:42:37.630Z
updated_time: 2022-01-14T06:44:19.522Z
is_conflict: 0
latitude: 1.36730000
longitude: 103.80140000
altitude: 0.0000
author: 
source_url: 
is_todo: 0
todo_due: 0
todo_completed: 0
source: joplin-desktop
source_application: net.cozic.joplin-desktop
application_data: 
order: 1642128157630
user_created_time: 2022-01-14T02:42:37.630Z
user_updated_time: 2022-01-14T06:44:19.522Z
encryption_cipher_text: 
encryption_applied: 0
markup_language: 1
is_shared: 0
share_id: 
conflict_original_id: 
master_key_id: 
type_: 1