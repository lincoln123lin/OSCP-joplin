id: f746988e0dfd4a458db3e8cb0bcffb3e
parent_id: 21e6d72f57e74d579fd78d0a2c478cc4
item_type: 1
item_id: 8ceefc0c650f4adbb0c0023984623b15
item_updated_time: 1643597365956
title_diff: "[]"
body_diff: "[{\"diffs\":[[0,\"16b7728)\"],[1,\"\\\n\\\n![bc1565b125b6948c6e04bc9f6577eb96.png](:/b4ced5cbeae746818757112f88f61167)\\\n\\\n# Domain Controller Synchronisation\\\n\\\nSteal all the password hashes for all admin users in the domain (use mimikatz and dump all the password hash of every user, or steal a copy of the NTDS.dit DB file)\\\n\\\n- Leaves a access trail;\\\n- May require us to upload tools to the server\\\n\\\nAlternative way is to abuse AD functionality to capture hashes remotely from a workstation\\\n\\\nIn production env, domains usually have more than one DC to provide redundancy. A DC may request an update for a specific object (e.g. account) with the IDL_DRSGetNCChanges API\\\n\\\n- DC receiving the request does not verify the request came from where; only associates SID has appropriate privileges\\\n- Can use a member of Domain Admins to request and it will succeed\\\n\\\n![dc0d21d90e4f78c0f18b834571bbda16.png](:/bc39b5c59a9f4d2a804a0ee4f59550dc)\\\n\\\n> lsadump::dcsync /user:&lt;username&gt;\"]],\"start1\":1196,\"start2\":1196,\"length1\":8,\"length2\":937}]"
metadata_diff: {"new":{},"deleted":[]}
encryption_cipher_text: 
encryption_applied: 0
updated_time: 2022-01-31T02:53:37.366Z
created_time: 2022-01-31T02:53:37.366Z
type_: 13