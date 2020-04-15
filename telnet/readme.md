# Telnet 설치 및설정

``` bash
sudo apt-get install xinetd
```

``` bash
sudo apt-get install telnetd
```

``` bash
cd /etc/xinetd.d
sudo vim telnet
```

``` bash
service telnet
{
 disable = no
 flags = REUSE
 socket_type = stream
 wait = no
 user = root
 server = /usr/sbin/in.telnetd
 log_on_failure += USERID
}
```
