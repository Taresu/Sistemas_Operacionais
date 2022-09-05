## Minhas resoluções:

#### 1)

![image](https://user-images.githubusercontent.com/83923976/188346496-1d7cf04e-fc6e-49a1-91eb-d919eb6ca8f4.png)

```bash
$  pgrep rsyslogd
868
$  renice -n -10 868
```

_______________________________________________________________________________________________________________________________________________________________________

#### 2)

![image](https://user-images.githubusercontent.com/83923976/188346507-5c8e1c2c-ac17-4f9c-80f8-b782f6df4f48.png)

```bash
$  touch ~/Exercicio/resultado-top-.out | sudo nice -n 19 & < top& -d 10
```
