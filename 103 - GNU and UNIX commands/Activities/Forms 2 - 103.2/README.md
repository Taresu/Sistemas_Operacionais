## Minhas resoluções:

##### 1)

![F2Q1](https://user-images.githubusercontent.com/83923976/186946343-3bcc0478-0a24-497c-9f60-ce8d1dc611d6.png)

```bash
$   tail -n 15 /etc/passwd | sort -n -t ':' -k3 | cut -d: -f1,3
```

##### 2)

![image](https://user-images.githubusercontent.com/83923976/186946492-899eb2b4-d7d1-4404-8cde-3384efca2dab.png)

```bash
$   cat /etc/passwd | grep -v daemon | wc -l
```
