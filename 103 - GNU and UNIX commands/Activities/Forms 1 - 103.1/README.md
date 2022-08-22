## Minhas resoluções:

O caminho completo do arquivo .bash_history para o seu usuário:
```bash{r, echo=FALSE}
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
```bash{r, echo=FALSE}
$   uname -r
5.15.0-46-generic
$   uname --kernel-release
5.15.0-46-generic
```
__________________________________________________________________
Os diretórios incluídos em seu PATH:
```bash{r, results='hide'}
$   ls
Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Vídeos
```
OU
```bash{r, echo=FALSE}
$   ls -a    
.              .bashrc  Documents  .mozilla  Public        Videos
..             .cache   Downloads  Music     snap
.bash_history  .config  .lesshst   Pictures  Templates
.bash_logout   Desktop  .local     .profile  .thunderbird
```
**OBS:** o dash '-a' mostra todos os arquivos e diretórios, incluindo os ocultos.
__________________________________________________________________
O hostname da máquina:
```bash{r, echo=FALSE}
$   uname -n
rle-202
```
OU
```bash{r, echo=FALSE}
$   uname --nodename
rle-202
```
__________________________________________________________________
O PID da sua sessão shell atual:
```bash{r, echo=FALSE}
$   pidof bash
7831
```
__________________________________________________________________
A localização do comando tar:
```bash{r, echo=FALSE}
$   type tar
tar is /usr/bin/tar
```
