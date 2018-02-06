# fr-commission-securite-cloud
FR - Supports de présentation en français pour la commission sécurité &amp; cloud, Telecom-Valley

## Diaporama de présentation

Document unique : [Commission sécurité cloud.pdf](https://github.com/ledroide/fr-commission-securite-cloud/Commission%20s%C3%A9curit%C3%A9%20cloud.pdf)

## Sources et documentation

Les études et documents cités sont sur [presentations/sources](https://drive.google.com/open?id=1P9nut3-c6ZVQW_wc_Klq0owCwjO4A8zG)

## Démonstrations

```bash
~ $ docker exec mysql-wp ps auxwww 
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
mysql        1  0.0  1.2 1270632 201020 ?      Ssl  09:46   0:01 mysqld
root        63  0.0  0.0  17504  2048 ?        Rs   10:36   0:00 ps auxwww

root@eb78198a1832:/# ls /sys/devices/

root@5b93404b19fd:/var/www/html# cat /proc/net/arp 
IP address       HW type     Flags       HW address            Mask     Device
10.32.0.2        0x1         0x2         02:42:0a:20:00:02     *        eth0
10.32.0.1        0x1         0x2         02:42:d5:c5:5d:39     *        eth0
root@5b93404b19fd:/var/www/html# hostname -I
10.32.0.4

root@eb78198a1832:/# cat /proc/net/fib_trie
           +-- 10.32.0.0/29 2 0 2
Hosts/Net: 6

root@5b93404b19fd:/var/www/html# egrep ^10 /etc/hosts
10.32.0.2       mysql fabe9f6fd32c mysql-wp
10.32.0.4       5b93404b19fd

root@eb78198a1832:/# ssh -l ecisse 10.32.0.1
ecisse@10.32.0.1's password: 
Welcome to Ubuntu 17.10 (GNU/Linux 4.13.0-21-generic x86_64)

ecisse@D20854-Gailuron:~$ id
uid=1002(ecisse) gid=1002(ecisse) groups=1002(ecisse),999(docker)
ecisse@D20854-Gailuron:~$ sudo -l
[sudo] password for ecisse: 
Sorry, user ecisse may not run sudo on D20854-Gailuron.
ecisse@D20854-Gailuron:~$ docker ps
CONTAINER ID        IMAGE                    COMMAND             CREATED             STATUS              PORTS               NAMES
eb78198a1832        rastasheep/ubuntu-sshd   "bash"              15 minutes ago      Up 15 minutes       22/tcp              confident_panini

~ $ mkdir -p Downloads/install/gitlab

~ $ docker run -ti --rm -v $HOME/Downloads/install/gitlab:/toto debian:wheezy bash
root@dada2cc8a000:/#
root@dada2cc8a000:/# cp /bin/sh /toto/gitlab-ci.install.bin
root@dada2cc8a000:/# chmod a+s /toto/gitlab-ci.install.bin
root@dada2cc8a000:/# exit
jujube@D20854-Gailuron:~$ ./Downloads/install/gitlab/gitlab-ci.install.bin 
# id -un
root
# 
```
