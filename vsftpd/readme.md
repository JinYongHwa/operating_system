
``` bash
 local_enable=YES               #로컬계정 사용자들의 접속 허용 
 write_enable=YES               #FTP 전송명령어 중 write를 허용여부  
 local_umask=022                #업로드 된파일의 권한 MASK
 idle_session_timeout=600       #접속 세션 유지 시간(초)  
 chroot_local_user=NO           #최상단 디렉토리를 접속한 유저 홈디렉토리로 제한
 allow_writeable_chroot=YES     #chroot_local_user 제한 설정할 경우 설정값
 chroot_list_enable=YES         #chroot_list_file(접속 허용 계정 리스트) 활용 여부
 listen=YES                     #standalone 설정 여부
 use_localtime=YES              #서버시간으로 사용
 local_max_rate=500000          #유저 전송속도 제한 bps
 force_dot_files=YES            #. 파일 표시 여부
 max_clients=10                 #최대 접속 허용수
 max_per_ip=2                   #한 아이피당 접속 허용수
```
