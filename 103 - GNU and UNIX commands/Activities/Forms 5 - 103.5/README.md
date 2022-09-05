## Minhas resoluções:

#### 1)

![image](https://user-images.githubusercontent.com/83923976/188346311-b9b53ce0-0afb-4009-a50c-cbd4b118cb34.png)

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

![image](https://user-images.githubusercontent.com/83923976/188346358-3ff69719-e5e7-44fb-a23e-e451b7255493.png)

```bash
$  mkdir ~/Exercicios/resultado-top.out
$  nohup watch -n 10 top & > ~/Exercicios/resultado-top.out
```

_______________________________________________________________________________________________________________________________________________________________________

#### 3)

![image](https://user-images.githubusercontent.com/83923976/188346369-de9388b3-2345-454d-8fab-cfa3beae120f.png)

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
