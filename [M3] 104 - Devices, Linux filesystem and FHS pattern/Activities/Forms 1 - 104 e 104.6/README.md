## Minhas resoluções:

### 1)

![image](https://user-images.githubusercontent.com/83923976/188508248-644e50c6-6fb6-40f2-9640-a0e2e7961cad.png)

```bash
#  fdisk /dev/sdX
```
1) Criar partição apertando a tecla "n"
2) Selecionar partição primária com "p"
3) Alternar partição com o número da partição respectiva (1-4)
4) Entrar com o tamanho da partição em 'Last sector' (+3G, +2G, +500M, +1500M, +2G e restante do disco por último p/ partição 4)
5) Escrever cada partição no disco com a tecla "w"

OBS: Após criar todas as partições, montar disco com 'mount -a'!

Para redimensionar a partição de número 7 (usando o GNU Parted):
```bash
#  parted /dev/sdX7
(parted) resizepart 7 3G
Warning: Shrinking a partition can cause data loss, are you sure
you want to continue?

Yes/No? y
```

Para definir a partição sdX5 como área de swap:
```bash
#  mkswap /dev/sdX5
```

Para formatar as partições 1 e 3 como ext4, a 6 como XFS e a 7 como Btrfs:
```bash
#  mkfs -t ext4 /dev/sdX1
#  mkfs -t ext4 /dev/sdX3
#  mkfs -t xfs /dev/sdX6
#  mkfs -t btrfs /dev/sdX7
```
___________________________________________________________________________________


### 2)

![image](https://user-images.githubusercontent.com/83923976/188508255-b8b402c3-3391-4d45-b34b-84685190810e.png)

O comando df fornece uma lista de todos os sistemas de arquivos disponíveis (já montados) em seu sistema, incluindo o tamanho total, quanto espaço foi usado, quanto espaço está disponível, a **porcentagem de uso** e onde estão montados. 

1) Para mostrarmos apenas a porcentagem de uso da partição root:
```bash
#  df -h --output=pcent /
```

Com o comando "p" (print), dentro de fdisk, é possível descobrir quanto espaço está disponível no disco. O espaço livre total será mostrado como a última linha de informação antes da própria tabela de partição.

2) Mostrar o uso de cada subdiretório e, em seguida, o uso total do diretório atual, incluindo subdiretórios
```bash
$  du -h /var1
```

3) Verificando o número de blocos existentes (em blocos de 1K):
```bash
$  df
```

Existem dois comandos que podem ser usados para verificar quanto espaço está sendo usado e
quanto resta em um sistema de arquivos. O primeiro é du, que significa “disk usage” (uso do disco).

Exemplo:
```bash
$  du
4816
$  du -h
4.8M
```

4) Executando as instruções do exercício:
```bash
$  e2label /dev/sdX1 "Particao 1"
$ tune2fs -i 7d /dev/sdX3
$ tune2fs -m 1 /dev/sdX3
$ e2label /dev/sdX6 "Exercicio"
```

5) Para checar o sistema de arquivos das partições 1, 3 e 6:
```bash
$  fsck /dev/sdX1
$  fsck /dev/sdX3
$  fsck /dev/sdX6
```
___________________________________________________________________________________


### 3)

![image](https://user-images.githubusercontent.com/83923976/188508265-40a95f5a-4e77-46cf-bddb-e02df170727c.png)

1)
```bash
$  touch /mnt/diretorio_temp
$  mount -t ext4 /dev/sdX3 /mnt/diretorio_temp
```

2) 
```bash
$  echo "/dev/sdX5 /mnt/diretorio_temp defaults 0 0" >> /etc/fstab
$  echo "swap /dev/sdX6 /mnt/diretorio_temp defaults 0 0" >> /etc/fstab
$  echo "/tmp /mnt/diretorio_temp defaults 0 0" >> /etc/fstab
```

3)
```bash
$  umont /dev/sdX3
```

4) ???
```bash
$  echo "/var /dev/sdX1 defaults 0 0" >> /etc/fstab
```
___________________________________________________________________________________

### 4)

![image](https://user-images.githubusercontent.com/83923976/188508275-5b6a7ddf-80a9-4c1e-bfa0-872e8f3263c9.png)

```bash
-rw-rw-r--    1 root root    0 Abr 26 17:17 Exerc1 
-rwsrwxr-x 1 root root    0 Abr 26 17:17 Exerc2 
-rwxrwxr--  1 root root    0 Abr 26 17:17 Exerc3 
drwxrwxr-x 2 root root 4096 Abr 26 17:17 Dir1 
drwxr-x---    2 root root 4096 Abr 26 17:17 Dir2
```

1)
```bash
$  mkdir -p /home/Permissoes
$  cd /home/Permissoes
$  touch Exerc1 Exerc2 Exerc3
$  mkdir Dir1 Dir2
```

```bash
$ chmod 364 /home/Permissoes/Exerc1
$ chmod 775 /home/Permissoes/Exerc2
$ chmod 774 /home/Permissoes/Exerc3
$ chmod -R 775 /home/Permissoes/Dir1
$ chmod -R 750 /home/Permissoes/Dir2
```

2)
```bash
#  chown usuario1:root Exerc1
#  chown usuario1:grupo1 Exerc2
#  chown root:root Exerc3

#  useradd lpi1
#  groupadd lpi1

# chown lpi1:lpi1 Dir1
# chown usuario1:grupo1 Dir2
```

3)
```bash
#  umask u=rw,g=r
Voltando ao final do exercício 2: 
#  umask u=rwx,g=rx,o=rx
```
___________________________________________________________________________________

### 5)

![image](https://user-images.githubusercontent.com/83923976/188508281-8e92771f-8082-409c-a164-dc4c95fe007c.png)
```
$  ln -s /boot/5.10.16.3-microsoft-standard-WSL2 kernel-boot
```
