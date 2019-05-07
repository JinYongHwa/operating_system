# Nginx란?
전통적으로 웹서버는 보통 아파치를 써왔으나 동시접속 1만이 되면 다운되는 문제점을 발견한 한 러시아 개발자가 NginX(엔진엑스)라는 새로운 웹서버를 개발함
네이버,넷플릭스,페이스북,GitHub 등 많은 메이저 사이트들이 Nginx 웹서버로 서비스되고 있어 안정성면에서 검증받은 서버


## Nginx 설치
``` bash
sudo apt-get install nginx
```

## Nginx 실행
``` bash
sudo service nginx start
```


## Nginx 종료
``` bash
sudo service nginx stop
```

## Nginx 설정파일 경로
/etc/nginx/nginx.conf

## Nginx 설정 변경
``` bash
sudo service nginx reload
```


# Nginx를 이용한 부하분산

![Nginx를 이용한 부하분산](https://github.com/JinYongHwa/operating_system/raw/master/nginx/Load-Balancer-Performance-With-SaltStack-And-Nginx.jpg)
[이미지출처](https://www.opcito.com/blogs/improve-your-load-balancer-performance-with-saltstack-and-nginx-2/)






### Core 모듈
```
user  nginx; # (디폴트값 : www-data) 
worker_processes  1;
error_log  /var/log/nginx/error.log warn;
pid        /var/run/nginx.pid;
```

user : NGINX 프로세스가 실행되는 권한
nginx는 마스터(master)와 워커(worker) 프로세스로 나뉜다.
워커 프로세스가 실질적인 웹서버 역할을 수행한다.
user 지시어는 워커 프로세스의 권한을 지정한다.
워커 프로세스를 악의적 사용자가 제어하면 해당 머신을 최고 사용자의 권한으로 원격제어하는 것이기 때문에 위험하다.
본 포스팅에서는 nginx로 변경하였다.

work_processes : NGINX 프로세스 실행 가능 수
위에서 언급한 워커 프로세스이다. 실질적인 웹서버 역할을 한다.
auto도 무방하지만, 명시적으로 서버에 장착되어 있는 코어 수 만큼 할당하는 것이 보통이며, 더 높게도 설정 가능하다.

pid : NGINX 마스터 프로세스 ID 정보가 저장된다.


### events 블락
```
events { 
    worker_connections  1024;
    # multi_accept on; (디폴트값 : off) 
}
```

NGINX의 특징인 비동기 이벤트 처리 방식에 대한 옵션을 설정한다.

worker_connections는 하나의 프로세스가 처리할 수 있는 커넥션의 수를 의미한다.

최대 접속자수 = worker_processes X worket_connections가 된다.


### http 블락
```
http { 
    include       /etc/nginx/mime.types;
    default_type  application/octet-stream;
 
    log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
    '$status $body_bytes_sent "$http_referer" '
    '"$http_user_agent" "$http_x_forwarded_for"';
 
    access_log  /var/log/nginx/access.log  main;
 
    sendfile        on;
 
    #tcp_nopush     on; 
 
    keepalive_timeout  65;
 
    #gzip  on; 
 
    include /etc/nginx/conf.d/*.conf;
}
```

keepalive_timeout : 접속시 커넥션을 몇 초동안 유지할지에 대한 설정값. 이 값이 높으면 불필요한 커넥션(접속)을 유지하기 때문에 낮은값 또는 0을 권장한다. (default=10)

servers token : NGINX의 버전을 숨길것인가에 대한 옵션이다. 보안상 주석을 제거하여 설정하는 것이 좋다.

types_hash_max_size, server_names_hash_bucket_size 호스트의 도메인 이름에 대한 공간을 설정하는 것으로 이 값이 낮을 경우 많은 가상 호스트 도메인을 등록한다거나, 도메인 이름이 길 경우 bucket 공간이 모자라 에러가 생길 수 있으므로 넉넉하게 설정한다.



[Nginx 설정예제](https://www.nginx.com/resources/wiki/start/topics/examples/full/)


참고링크
- https://opentutorials.org/module/384/3462
- https://extrememanual.net/9976
