# Tratamiento de la TTY postExplotacion

+ __Generar una shell Bash con python2 y 3__


```bash
python -c 'import pty; pty.spawn("/bin/bash")'
```
```bash
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

+ __Generar una shell Bash con script__
```bash
script /dev/null -c bash
```

+ __Configurar y ajustar la terminal__
```bash
stty raw -echo; fg; ls; export SHELL=/bin/bash; export TERM=screen; stty rows 38 columns 116; reset;
```

```bash
stty raw -echo;fg 
reset
xterm
export TERM=xterm-256color
export SHELL=bash
source /etc/skel/.bashrc
stty rows 50 cols 200
```