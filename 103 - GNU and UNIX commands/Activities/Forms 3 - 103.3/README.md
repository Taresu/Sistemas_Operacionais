## Minhas resoluções:

##### 1)

![image](https://user-images.githubusercontent.com/83923976/186947678-fee99ea5-95b9-40f9-a426-7cf5f3f4ad15.png)

Input:
```bash
$  mkdir LPI1 /home/tsalata 
$  mkdir Aulas Exercicios Exemplos /home/tsalata/LPI1 
$  ls /home/tsalata/LPI1
```
Output:
```
Aulas   Exercicios   Exemplos
```

_______________________________________________________________________________________________________________________________________________________________________

##### 2)

![image](https://user-images.githubusercontent.com/83923976/186947696-f8825903-fbf8-4400-beef-eecd6e0dd192.png)

Input:
```bash
$  mkdir home/tsalata/LPI1/Exercicios/Network
$  cp /etc/Network/* LPI1/Exercicios/Network/ -r
$  ls /LPI1/Exercicios/Network
```

Output:
```
if-down.d   if-post-down.d   if-pre-up.d   if-up.d
```

_______________________________________________________________________________________________________________________________________________________________________

##### 3)

![image](https://user-images.githubusercontent.com/83923976/186947774-5323397d-9bcf-4de1-93c5-dae59dcde5f4.png)

Input:
```bash
$  mkdir -p LPI1/Exercicios/Config
$  sudo cp $(sudo find /etc/* -name "*.conf") "LPI1/Exercicios/Config"
$  ls LPI1/Exercicios/Config/
```

Output:
```
10-antialias.conf
10-autohit.conf
10-console.conf
[...]
```
OBS: Muitos arquivos são mostrados (com o programa / comando tree conseguimos quantifica-los)
```bash
$  sudo apt install tree (no Ubuntu)
$  cd LPI1/Exercicios/Config/
$  tree 
[...]
I
L__ xerox_mfp.conf
0 directories, 347 files
```
_______________________________________________________________________________________________________________________________________________________________________


##### 4)

![image](https://user-images.githubusercontent.com/83923976/186947793-251e21d4-02bd-4985-abcc-af4e690151c9.png)

```bash
$  sudo find /etc -name "cron"
/etc/default/cron
/etc/init.d/cron
/etc/pam.d/cron
$  sudo gzip -r $(sudo find /etc/* -name "cron")
$  ls
arquivos-cron-tgz   Config   Network
#  gzip -f arquivos-cron-tgz
/etc/default/cron
/etc/init.d/cron
/etc/pam.d/cron
```

##### 5)

![image](https://user-images.githubusercontent.com/83923976/186947838-0910fd9f-9ee7-43ed-bbc2-4f0486d2566b.png)

```bash
$  mkdir /LPI1/Exercicios/Descompactar/
$  cd /LPI1/Exercicios/
$  gunzip arquivos-cron.tgz /LPI1/Exercicios/Descompactar/
```

##### 6)

![image](https://user-images.githubusercontent.com/83923976/186947860-743c1972-11f3-4db1-919b-0ed48381f9b9.png)

```bash
$  sudo find /var -name "*.gz" -mtime 2
```
