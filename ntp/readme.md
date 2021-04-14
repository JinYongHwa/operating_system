# NTP 서버란?
> 네트워크 타임 프로토콜(Network Time Protocol)
NTP(Network Time Protocol)은 지연이 있을 수 있는 네트워크 상에서, 컴퓨터와 컴퓨터간의 시간을 동기화 하기 위한 네트워크 프로토콜이다. 

(https://upload.wikimedia.org/wikipedia/commons/thumb/8/8d/NTP-Algorithm.svg/1920px-NTP-Algorithm.svg.png)




###  ntp 서버설치
``` bash
sudo apt-get install ntp
```

### NTP Pool
https://www.ntppool.org/ko/


### ntp 서버 시장
``` bash
sudo service ntp reload 
```

### ntp 확인하기
``` bash
sudo ntpq -p
```
