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

### adduser [사용자 이름]
사용자를 추가한다

### whoami
현재 접속된 사용자 정보를 알려준다

### passwd
현재 접속된 사용자의 패스워드를 변경한다

### sudo passwd [사용자명]
특정 사용자의 패스워드를 변경한다


### chmod [권한값] [파일/디렉토리명]
특정 파일이나 디렉토리의 접근권한을 변경함

```
ex)  drwxr-xr-x
```
```
- 1필드 : 타입 
     '- 인 경우 : 파일
     d 인 경우 : 디렉토리
     | 인 경우 : 다른 파일을 가리키는 링크
     p 인 경우 : pipe. 두 개의 프로그램을 연결하는 파이프 파일.
     b 인 경우 : block device. 블럭 단위로 하드웨어와 반응하는 파일
     c 인 경우 : character device. 스트림 단위로 하드웨어와 반응하는 파일
```

- 2-4필드 : 소유주 (USER) 권한
- 5-7필드 : 그룹 (Group) 권한
- 8-10필드 : 나머지 (Others) 권한

- r : 읽기권한(read) = 4
- w : 쓰기권한(write) = 2
- x : 실행권한(eXecute) = 1
- - : 권한 없음 설정 = 0

### chown [소유자(:그룹)] [파일/디렉토리명]
특정 파일이나 디렉토리의 소유자를 변경함
