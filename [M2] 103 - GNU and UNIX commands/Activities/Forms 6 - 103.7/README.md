## Minhas resoluções:

#### 1)

![image](https://user-images.githubusercontent.com/83923976/188346428-51669fa8-6f07-467b-9cb0-fd186ac6a8b4.png)

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

![image](https://user-images.githubusercontent.com/83923976/188346438-419cec7c-5625-4632-9153-bdd5e9ebf75d.png)

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

![image](https://user-images.githubusercontent.com/83923976/188346451-0b3599ca-4c33-47ce-b918-27145177b96c.png)

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

![image](https://user-images.githubusercontent.com/83923976/188346459-4334ad14-9a51-48a1-955e-f35d310bea3a.png)

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
