id: 0730fffabefb4d39a780b51edd5dce79
parent_id: 
item_type: 1
item_id: 9e69c5460e694bedb9ad12241aa72ae0
item_updated_time: 1651226358469
title_diff: "[{\"diffs\":[[1,\"UDP Scanning\\\r\"]],\"start1\":0,\"start2\":0,\"length1\":0,\"length2\":13}]"
body_diff: "[{\"diffs\":[[1,\"# UDP Scan:\\\n\\\n> nmap -sS -sU -Pn -sV 172.21.0.0\\\n> \\\n> nmap -sU -A --top-ports=20 --version-all\\\n> \\\n> nmap -sU -A -p 53,67,68,161,162 --version-all\\\n> \\\n> unicornscan -mU -p ,161,162,137,123,138,1434,445,135,67,68,53,139,500,637,162,69\\\n\\\n# Unique Services that uses UDP\\\n\\\nTFTP - Trivial File Transfer Protocol (UDP port 69)\\\n\\\n> \\\\# To communicate, use the tftp software\\\n> \\\n> Tftp 10.11.1.111\\\n> \\\n> binary\\\n> \\\n> verbose\\\n> \\\n> get \\\\\\\\PROGRA~1\\\\\\\\MICROS~1\\\\\\\\MSSQL1~1.SQL\\\\\\\\MSSQL\\\\\\\\Backup\\\\\\\\master.mdf\\\n> \\\n> \\\\# We then crack the hashes\\\n> \\\n> https://github.com/xpn/Powershell-PostExploitation\"]],\"start1\":0,\"start2\":0,\"length1\":0,\"length2\":566}]"
metadata_diff: {"new":{"id":"9e69c5460e694bedb9ad12241aa72ae0","parent_id":"6b8d3e46660447279f5aee899ce00b64","latitude":"1.36730000","longitude":"103.80140000","altitude":"0.0000","author":"","source_url":"","is_todo":0,"todo_due":0,"todo_completed":0,"source":"joplin-desktop","source_application":"net.cozic.joplin-desktop","application_data":"","order":0,"markup_language":1,"is_shared":0,"share_id":"","conflict_original_id":"","master_key_id":""},"deleted":[]}
encryption_cipher_text: 
encryption_applied: 0
updated_time: 2022-04-29T09:59:25.769Z
created_time: 2022-04-29T09:59:25.769Z
type_: 13