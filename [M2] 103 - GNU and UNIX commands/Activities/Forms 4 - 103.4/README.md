## Minhas resoluções:

#### 1)

![image](https://user-images.githubusercontent.com/83923976/187095978-dc4cc6af-09fe-4826-b37f-aae132949704.png)


**Input:**
```bash
$   touch diretorios-config.out
$   find /var name "*config*" -type d | xargs ls -ld > diretorios-config.out
$   cat diretorios-config.out
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

_______________________________________________________________________________________________________________________________________________________________________

#### 2)

![image](https://user-images.githubusercontent.com/83923976/187095986-55b539ef-342a-47dd-b067-a3835caabadb.png)


##### Canais de comunicação e redirecionadores:
**Entrada padrão** - stdin (0), representado por < ou <0 \
**Saída padrão** - stdout (1), representado por > ou 1> \
**Saída de erros** - stderr (2), representado por 2>

Em uma sessão comum de shell, o teclado é definido como stdin (0) e a tela do monitor como stdout (1) ou stderr (2).

##### Assumindo o fluxo de dados:
x <-> y

##### Redirecionadores de entradas e saídas e fluxo de dados:
**x > y arquivo:** sobrescreve uma saída y com dados de uma saída x (fluxo da esquerda para a direita); \
**x < y arquivo:** reatribui a fonte de entrada de um arquivo (fluxo da direita para a esquerda); \
**x >> y arquivo:**  adiciona dados de um arquivo x em y (sem sobrescrever); \
**x 2> y arquivo:** redireciona uma mensagem de erro (stderr) a um destino; \
**>x arquivo 2>&1 y:** redireciona o resultado da mensagem de erro (stderr) para a saída padrão y (stdout) e logo em seguida, para o arquivo x.


_______________________________________________________________________________________________________________________________________________________________________

#### 3)

![image](https://user-images.githubusercontent.com/83923976/187095994-4e9d1e39-3f64-4469-991a-09eba3f9daeb.png)

**Input:**
```bash
$  ls -R ~/LPI1/Exercicios/Network < lista-network.out | tee lista-network.out |
$  ls -R ~/LPI1/Exercicios/Network > lista-network.out
```

**Output:**
```bash
home/tsalata/LPI1/Exercicios/Network:
if-down.d  if-post-down.d  if-pre-up.d  if-up.d

/home/tsalata/LPI1/Exercicios/Network/if-down.d:
avahi-autoipd  openvpn  wpasupplicant

/home/tsalata/LPI1/Exercicios/Network/if-post-down.d:
wireless-tools  wpasupplicant

/home/tsalata/LPI1/Exercicios/Network/if-pre-up.d:
ethtool  wireless-tools  wpasupplicant

/home/tsalata/LPI1/Exercicios/Network/if-up.d:
avahi-autoipd  ethtool  openvpn  wpasupplicant
```
_______________________________________________________________________________________________________________________________________________________________________
