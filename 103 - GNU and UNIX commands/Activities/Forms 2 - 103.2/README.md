## Minhas resoluções:

##### 1)
```bash
$   tail -n 15 /etc/passwd | sort -n -t ':' -k3 | cut -d: -f1,3
```

##### 2)
```bash
$   cat /etc/passwd | grep -v daemon | wc -l
```
