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
