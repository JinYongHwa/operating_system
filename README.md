## GitHub 주소
https://github.com/JinYongHwa/operating_system


## 참고 링크
- [우분투 한국 커뮤니티 포럼](https://forum.ubuntu-kr.org/index.php)
- [KLDP](https://kldp.org/)
- [ubuntu.com](https://www.ubuntu.com/)


## 명령어 정리

### sudo 
루트권한에 접근하기 위한 명령어

### sudo apt-get update
apt-get은 인덱스를 가지고 있는데 이 인덱스는 /etc/apt/sources.list에 있습니다. 이곳에 저장된 저장소에서 사용할 패키지의 정보를 얻습니다. 
 

### sudo apt-get upgade
설치되어 있는 패키지를 모두 새버전으로 업그래이드 합니다.

### sudo apt-get [패키지명]
특정 패키지 설치

### sudo apt-cache  search [패키지명]
패키지 검색


### cd [경로]
디렉토리 경로이동
> cd /home/ubuntu

> cd ..

### pwd
현재 디렉토리 위치 표시


### ls
현재 위치한 디렉토리의 전체 파일 표시


### mkdir [디렉토리명]
디렉토리 생성
> mkdir test


### touch [파일명]
파일 생성
> touch test

### cp [대상파일] [복사경로]
파일을 복사한다
> cp test /home/ubuntu
