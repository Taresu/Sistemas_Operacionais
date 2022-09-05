## Minhas resoluções:

#### 1)

**Input:**
```bash
$  cat /etc/passwd | egrep  ":[0-9]{3}$" | cut -d':' -f1
$  grep nologin$ /etc/passwd
```
**Output:**
```bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
[...]
geoclue:x:123:130::/var/lib/geoclue:/usr/sbin/nologin
pulse:x:124:131:PulseAudio daemon,,,:/run/pulse:/usr/sbin/nologin
```

_______________________________________________________________________________________________________________________________________________________________________

#### 2)

**Input:**
```bash
$  grep -rnwl '/etc/' -e 'eth0'
```
**Output:**
```bash
/etc/avahi/avahi-daemon.conf
/etc/dhcp/dhclient.conf
/etc/initramfs-tools/initramfs.conf
```

_______________________________________________________________________________________________________________________________________________________________________

#### 3)

![image](https://user-images.githubusercontent.com/83923976/187095994-4e9d1e39-3f64-4469-991a-09eba3f9daeb.png)

**Input:**
```bash
$   cat /etc/passwd | cut -d':' -f1,3 | egrep  ":[0-9]{3}$" | cut -d':' -f1
```

**Output:**
```bash
systemd-network
systemd-resolve
[...]
vboxadd
mysql
```
Para conferir se os ID's possuem 3 dígitos:

**Input:**
```bash
$   cat /etc/passwd | cut -d':' -f1,3 | egrep  ":[0-9]{3}$"
```

**Output:**
```bash
systemd-network:100
systemd-resolve:101
[...]
vboxadd:999
mysql:128
```


_______________________________________________________________________________________________________________________________________________________________________

#### 4)

**Input:**
```bash
$  cp Exercicios/Alunos.txt  Exercicios/Alunos-Exercicio.txt
$  sed -i 's/Ana \Maria/Marieta/g' Exercicios/Alunos-Exercicio.txt
```
OBS: Foi adicionado o nome "Ana Maria de Carvalho" em *Alunos.txt* para que a substuição de "Ana Maria" por "Marieta", fosse possível!

Para checar o conteúdo atualizado de *Alunos-Exercicio.txt*:
```bash
$  cat Exercicios/Alunos-Exercicio.txt
```

**Output:**
```bash
Alan Lima De Campos 
*Marieta* de Carvalho                                           <---
[...]
Joao Guilherme Martins Silva 
```