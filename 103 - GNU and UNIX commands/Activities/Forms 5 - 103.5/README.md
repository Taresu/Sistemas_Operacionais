## Minhas resoluções:

#### 1)

Instalando e iniciando htop (no Ubuntu):
```bash

$  sudo apt install htop
$  htop
```
**Output:**
```bash
drwxr-xr-x 2 root root 20480 ago 23 14:49 /var/cache/fontconfig
drwx------ 2 root root  4096 ago 23 13:23 /var/cache/ldconfig
drwxr-xr-x 3 gdm  gdm   4096 ago  9 08:51 /var/lib/gdm3/.config
drwxr-xr-x 2 root root  4096 ago  9 08:51 /var/lib/systemd/deb-systemd-helper-enabled/oem-config.service.wants
drwxr-xr-x 2 root root 12288 ago 23 14:49 /var/snap/firefox/common/fontconfig
drwxr-xr-x 2 root root  4096 ago 20 11:25 /var/snap/snapd-desktop-integration/common/fontconfig
drwxr-xr-x 2 root root  4096 ago 20 11:25 /var/snap/snap-store/common/fontconfig
```

#### **Informações**


```bash
Total de Memória RAM utilizada (em MB): 2.25G = 2250MB

Load Average (Média dos Últimos 5 minutos): 0.34
```

**OBS:** O campo Load Average mostra as cargas médias do sistema / processos no intervalo de 1min, 5min e 15min.
```bash
Quantidade de Processos em Execução: 154 tasks no total

PID dos 3 processos que estão utilizando mais Memória: 
# Para organizar os processos em uso de memória
Shift + M
1223, 1247, 1275
```

Para obter o PPID (Parent Process ID) dos 3 processos com maior tempo de uso de CPU:
1) Aperte a tecla **'f'**
2) Vá com as setas do teclado até encontrar o campo "PPID"
3) Aperte a tecla **'d'** para ativar o display do campo desejado
4) Saia da filtragem com a tecla **'q'**
**Shift + M** (no *top*)
1068, 1, 1068

_______________________________________________________________________________________________________________________________________________________________________

#### 2)

![image](https://user-images.githubusercontent.com/83923976/187095986-55b539ef-342a-47dd-b067-a3835caabadb.png)

```bash
$  mkdir ~/Exercicios/resultado-top.out
$  nohup watch -n 10 top & > ~/Exercicios/resultado-top.out
```

_______________________________________________________________________________________________________________________________________________________________________

#### 3)

![image](https://user-images.githubusercontent.com/83923976/187095994-4e9d1e39-3f64-4469-991a-09eba3f9daeb.png)

```bash
$  pgrep nohup watch -n 10 top
22515
$  kill -9 22515
[23]     Done                                      nohup watch -n 10 top
```

OU

```bash
$  pidof nohup watch -n 10 top
22515
$  kill -9 22515
[23]     Done                                      nohup watch -n 10 top
```
_______________________________________________________________________________________________________________________________________________________________________
