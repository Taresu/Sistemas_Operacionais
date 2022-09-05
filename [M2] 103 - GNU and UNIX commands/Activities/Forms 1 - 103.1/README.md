## Minhas resoluções:

#### 1)

![image](https://user-images.githubusercontent.com/83923976/186946777-4e3f8325-826a-485e-b545-885af6be3c0c.png)

O caminho completo do arquivo .bash_history para o seu usuário:
```bash
$   set | grep HISTFILE
$   sudo find /home -name ".bash_history" | xargs grep sudo
$   pwd
/home/rle-202
$   ls -a
.              .bashrc  Documents  .mozilla  Public        Videos
..             .cache   Downloads  Music     snap
.bash_history  .config  .lesshst   Pictures  Templates
.bash_logout   Desktop  .local     .profile  .thunderbird
```
__________________________________________________________________
O release do kernel instalado:
```bash
$   uname -r
5.15.0-46-generic
$   uname --kernel-release
5.15.0-46-generic
```
__________________________________________________________________
Os diretórios incluídos em seu PATH:
```bash
$   ls
Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Vídeos
```
OU
```bash
$   ls -a    
.              .bashrc  Documents  .mozilla  Public        Videos
..             .cache   Downloads  Music     snap
.bash_history  .config  .lesshst   Pictures  Templates
.bash_logout   Desktop  .local     .profile  .thunderbird
```
**OBS:** o dash '-a' mostra todos os arquivos e diretórios, incluindo os ocultos.
__________________________________________________________________
O hostname da máquina:
```bash
$   uname -n
rle-202
```
OU
```bash
$   uname --nodename
rle-202
```
__________________________________________________________________
O PID da sua sessão shell atual:
```bash
$   pidof bash
7831
```
__________________________________________________________________
A localização do comando tar:
```bash
$   type tar
tar is /usr/bin/tar
```
__________________________________________________________________

#### 2)

![image](https://user-images.githubusercontent.com/83923976/186946886-c7bc9802-643f-45ae-a34c-e2ef2096672c.png)

```bash
$   NOME="Thales Sgarbi Salata"
$   echo $NOME
Thales Sgarbi Salata
$   export NOME 
$   bash
$   echo $NOME
Thales Sgarbi Salata
```
__________________________________________________________________

#### 3)

![image](https://user-images.githubusercontent.com/83923976/186947419-47bda051-76e9-44d7-99fd-d10f5ca1fe08.png)

```bash
Assumindo a definição da variável $NOME do exercício 2), segue que:
$   alias frase='echo "O Conteúdo da Variável NOME é: Thales Sgarbi Salata"'
$   frase
O Conteúdo da Variável NOME é: Thales Sgarbi Salata
```
