20160804
전에 쓰던 노트북에 페도라19를 올려서 서버를 가동시키기 시작했다
내용엔 없지만 ssh와 디폴트 startx 시동 부분을 고쳤는데
ssh 는 chkconfig명령어를 사용해 부팅시 자동 시작하도록 하였고 
ui는 default target 을 cui 로 하였다

http 시동하는데 문제가 참 많았는데 보안상의 문제도 있었다
그리하여 selinux 와 firewall 를 죽였고 물론 iptables 도 죽였다
또한 /var/www/html 디렉토리가 기본적으로 권한이 주어지지 않아
chmod를 이용한 777권한을 무식하게 줬다
또한 ipv6로 설정되어있길레 http.conf 파일의 LISTEN 항목을 80 에서 0.0.0.0:80으로 수정하여 ipv4
로 설정하였다
php모듈을 사용하기 위한 php, php-common을 설치하였다
데이터베이스 서버도 설치해놨다
mariadb 를 쓴다
