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
