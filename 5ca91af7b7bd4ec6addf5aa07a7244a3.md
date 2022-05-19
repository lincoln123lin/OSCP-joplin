Pivoting/Tunneling

# Check if your tunnel is active and running:

- nc -z localhost <port>|| echo 'no tunnel open'</port>
- netstat -lpnt | grep <port>| grep ssh</port>
- ps aux | grep ssh

# SSH Tunneling

Note: Target must have SSH running for there service

1.  Create SSH Tunnel: ssh -D localhost: <local port="">-f -N user@localhost -p</local>
2.  Setup ProxyChains. Edit the following config file (/etc/proxychains.conf)
3.  Add the following line into the config: Socks5 127.0.0.1
4.  Run commands through the tunnel: proxychains <command></command>

## SSHuttle

In Kali

Source: https://github.com/sshuttle/sshuttle

- **sshuttle -r root@172.21.0.0 10.2.2.0/24**

**![9a4ed4cc714439b900bd1e27106e3577.png](:/8a73940cb76e420788f964c884e16a49)**

## To specify the port to use on localhost:

- sshuttle -l 127.0.0.1:8080 -r sean@10.11.1.251 10.1.1.0/24
    
    ![d0bd6488b791ddaee9efaf6ce98612a7.png](:/a37e7108b4694b1094df6400bdca3b81)
    

# Meterpreter

Use only if you have a meterpreter shell and you need to pivot to another network.

## Portfwd

- meterpreter > portfwd add -l 80 -r 172.21.0.0 -p 80

## Autoroute

In Metasploit

1.  use post/multi/manage/autoroute

```
msf5 post(multi/manage/autoroute) > options

Module options (post/multi/manage/autoroute):

   Name     Current Setting  Required  Description
   ----     ---------------  --------  -----------
   CMD      autoadd          yes       Specify the autoroute command (Accepted: add, autoadd, print, delete, default)
   NETMASK  255.255.255.0    no        Netmask (IPv4 as "255.255.255.0" or CIDR as "/24"
   SESSION                   yes       The session to run this module on.
   SUBNET                    no        Subnet (IPv4, for example, 10.10.10.0)

msf5 post(multi/manage/autoroute) > 
```

2.  set session
3.  run

## Metasploit Socks Proxy

1 auxiliary/server/socks4a normal No Socks4a Proxy Server
2 auxiliary/server/socks5 normal No Socks5 Proxy Server
3 auxiliary/server/socks_unc normal No SOCKS Proxy UNC Path Redirection

# Ncat

## Http Proxy

- ncat -vv --listen 3128 --proxy-type http

## Port Forwarder

1.  mknod pivot p
2.  nc -l -p &lt; port to listen on&gt; 0<pivot | nc <target><pivot-port>1>pivot</pivot-port></target>

# Cntlm

apt install cntlm

1.  cntlm -u username@breakme.local -I proxy
2.  export http://127.0.0.1:3128, export https://127.0.0.1:3128
3.  Accessing with browser: chromium --proxy-server="http://127.0.0.1:3128"

# netsh port forwarding

- netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=9000 connectaddress=192.168.0.10 connectport=80
- netsh interface portproxy delete v4tov4 listenaddress=127.0.0.1 listenport=9000

# Proxy Binaries for Windows

Windows 10 has SSH (Thanks WSL!)
plink.exe (In Kali)

# Other Tools:

- ssf: https://github.com/securesocketfunneling/ssf
- rpivot: https://github.com/klsecservices/rpivot
- hans (ICMP Tunneling): http://code.gerade.org/hans/
- Iodine (ICMP Tunneling over DNS): https://code.kryo.se/iodine/
- Dnscat2: https://github.com/iagox86/dnscat2
- Chisel: https://github.com/jpillora/chisel
- httptunnel: In Kali apt install httptunnel
- ligolo: https://github.com/sysdream/ligolo
- reGeorg: https://github.com/sensepost/reGeorg

# Other Resources:

- https://0xdf.gitlab.io/2019/01/28/pwk-notes-tunneling-update1.html
- https://highon.coffee/blog/ssh-meterpreter-pivoting-techniques/
- https://medium.com/maverislabs/proxyjump-the-ssh-option-you-probably-never-heard-of-2d7e41d43464

id: 5ca91af7b7bd4ec6addf5aa07a7244a3
parent_id: fa5212f3e7624b48b87153f3e4182dd1
created_time: 2020-04-15T18:52:38.528Z
updated_time: 2022-05-05T02:36:59.084Z
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
order: 0
user_created_time: 2020-04-15T18:52:38.528Z
user_updated_time: 2022-05-05T02:36:59.084Z
encryption_cipher_text: 
encryption_applied: 0
markup_language: 1
is_shared: 0
share_id: 
conflict_original_id: 
master_key_id: 
type_: 1