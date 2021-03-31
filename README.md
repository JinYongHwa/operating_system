## GitHub 주소
https://github.com/JinYongHwa/operating_system

## Email 주소
yhjin@hhsoft.co.kr


## 참고 링크
- [우분투 한국 커뮤니티 포럼](https://forum.ubuntu-kr.org/index.php)
- [KLDP](https://kldp.org/)
- [ubuntu.com](https://www.ubuntu.com/)


# 명령어 정리





## 패키지 설치관련 명령어

### sudo apt-get update
apt-get은 인덱스를 가지고 있는데 이 인덱스는 /etc/apt/sources.list에 있습니다. 이곳에 저장된 저장소에서 사용할 패키지의 정보를 얻습니다. 
 

### sudo apt-get upgade
설치되어 있는 패키지를 모두 새버전으로 업그래이드 합니다.

### sudo apt-get install [패키지명]
특정 패키지 설치

### sudo apt-cache  search [패키지명]
패키지 검색



## 파일/디렉토리 관련 명령어

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


### cat [파일명]
특정 파일의 내용을 Output 으로 출력함

### echo [텍스트]
특정 텍스트를 Output 으로 출력함

### [output] > [파일명]
output 의 내용을 해당 파일에 덮어씌움

### [output] >> [파일명]
output 의 내용을 해당 파일내용의 끝에 붙여넣음


### head [파일명]
파일의 처음 부분을 출력함

### tail [파일명]
파일의 마지막 부분을 출력함


### tar -cvf [파일명.tar] [폴더명]
폴더의 내용을 패키지로 묶어준다

### tar -xvf [파일명.tar]
패키지로 묶은 파일을 풀어준다

### tar -zcvf [파일명.tar.gz] [폴더명]
폴더의 내용을 압축해 패키지로 묶어준다

### tar -zxvf [파일명.tar.gz]
tar.gz 파일의 압축을 풀어준다

## 사용자/ 관련 명령어

### sudo 
루트권한에 접근하기 위한 명령어


### adduser [계정이름]
사용자를 추가한다

### whoami
현재 접속된 사용자 정보를 알려준다

### passwd
현재 접속된 사용자의 패스워드를 변경한다

### sudo passwd [계정이름]
특정 사용자의 패스워드를 변경한다


### chmod [권한값] [파일/디렉토리명]
특정 파일이나 디렉토리의 접근권한을 변경함

```
ex)  drwxr-xr-x
```


- 2-4필드 : 소유주 (USER) 권한
- 5-7필드 : 그룹 (Group) 권한
- 8-10필드 : 나머지 (Others) 권한

- r : 읽기권한(read) = 4
- w : 쓰기권한(write) = 2
- x : 실행권한(eXecute) = 1
- -: 권한 없음 설정 = 0

### chown [소유자(:그룹)] [파일/디렉토리명]
특정 파일이나 디렉토리의 소유자를 변경함

## 네트워크 관련 명령어

### wget [URL]
해당 URL 의 내용을 네트워크로부터 받아온다




## 시스템 관련 명령어

### df
디스크 용량확인

### du
현재 디렉토리의 용량확인

### ps
리눅스에서 실행중인 프로세스 목록확인

### top
리눅스에 실행중인 프로세스의 cpu 점유율 및 메모리 사용량을 모니터링 할수 있는 명령어

### free
리눅스의 SWAP 메모리 용량확인

## crontab
윈도우의 예약된 작업과 같이 리눅스에 주기적인 작업을 시킬때 사용

## crontab -e
크론탭을 편집기 실행

## crontab -l
크론탭에 등록된 명령어리스트를 보여줌

```
*　　　　　　*　　　　　　*　　　　　　*　　　　　　*
분(0-59)　　시간(0-23)　　일(1-31)　　월(1-12)　　　요일(0-7)
```

# 프로세스 관련 명령어

### ps -ef
현재 리눅스에서 실행중인 프로세스목록을 보여줌

### kill -9 [프로세스번호]
특정 프로세스 종료


# 리눅스 환경변수
- SHELL: 커맨드쉘 프로그램의 경로, 기본으로 bash shell을 이용한다 (/bin/bash)
- TERM: 현재 터미널 프로그램의 정보
- USER: 사용자의 이름
- UID: 현재 사용자의 UID
- LS_COLORS: 색 코드를 이용하여 커맨드 창에 색깔을 나타내는 환경변수이다.
- MAIL: 사용자의 메일이 저장되는 위치
- PATH: 프로그램을 실행시킬 때, 실질적으로 프로그램이 위치하고 있는 장소들을 모은 환경 변수
- PWD: 현재 작업 디렉토리
- LANG: 언어 설정을 위한 환경변수
- HOME: 현재 사용자의 홈 디렉토리
- OLDPWD: 이전 작업 디렉토리
- PS1: 쉘 세션의 모양을 정의한다.
- PS2: 명령어가 여러줄에 걸져 있을 경우 모양을 정의한다.
- _: 가장 최근에 실행한 명령어
- OSTYPE: os의 타입 (centos는 linux-gnu)
- HISTFILESIZE: 히스토리 기록의 최대 라인 수

### export
환경변수를 등록하는 명령어
``` bash
export NAME="JINYONGHWA"
echo $NAME
```

# Bash Shell

### ~/.bashrc
새터미널창을 열거나 로그인 했을때 실행되는 파일

### ~/.bash_logout
사용자가 로그아웃 하였을때 실행되는 


### hello.py
``` python
import time
while True:
 time.sleep(3)
 print("hello")
```

### hello.sh
``` bash
while : 
do 
 echo "hello" 
 sleep 1 
 done

```
