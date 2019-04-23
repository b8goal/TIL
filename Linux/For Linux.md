## su (switch user) 명령어
- 현재 계정을 로그아웃 하지 않고 다른 계정으로 전환하는 명령어
```bash
su
// su [user_name], su root 사용자로 변경 -> root 암호를 임력해야 한다

su user 01
// 다른 사용자로 변경한다

su - user01
// 다른 사용자로 변경하면서 환경변수까지 적용한다. (su, su - 차이)

whoami
// 현재 사용자를 확인한다

logout (또는 exit)
// 이전 계정으로 돌아온다

su -c 'apt-get update'
// root 권한으로 하나의 명령만 실행한다
``` 

## 우분투(Ubuntu) 에서 pip & pip3 설치(install) 방법
- pip 이란 python으로 작성된 패키지의 설치 및 관리를 해주는 프로그램
- pip을 이용하면 의존성 문제를 자동적으로해결해주기 때문에 편리하다
- pip은 python 2.x, pip3는 python 3.x 프로그램
```
apt-get install python-pip
apt-get install python3-pip
```

## 리눅스에서 git 설치
```bash
apt-get install git
```

## 파일 압축하기
```
tar -cf my_file.tar myfile.txt myile.dat
```
 - -c : 압축파일 만들기
 - -f : 파일(tar은 원래 테이프 백업용으로 만들진 s/w이다. 파일을 다룰 때는 -f 옵션이 필요)
 - 옵션을 조합할 때 -cf라고 하면 오류가 발생. 뒤에 인자ㅗ 들어간 my_ile.tar가 -f 옵션과 연결되어야 하기 때문이다.

 - 용량 절약을 위해 gzip 압축이나 bzip 압축을 추가하고 싶다면 아래와 같이 -z 또는 -j 옵션을 사용하자.
```
tar -czf my_file.tar.gz myfile.txt myfile.dat
tar -cjf my_file.tar.gz2 myile.txt myfile.dat
```
 - -z : gzip 사용(tar.gz 파일)
 - -j : bzip 사용(tar.gz2 파일)

## 특정 디렉토리에 있는 파일을 압축하기
 - ~/my_dr 디렉토에 있는 txt 파일을 압축

```
tar -czf myfle.tar.gz ~/my_dir/*.txt
```
 - ~my_dir 디렉토리로 간 후, txt파일을 압축
```
tar -czf myfile.tar.gz -C ~/my_dir *.txt
```

 - -C [디렉토리] : 디렉토리 변경(압축 경로 지정)

 - -t : 압축 파일 내용 표시
 - -v : 파일명어 이외에 오양 등 좀 더 자세한 정보를 보고 싶다면 -v 옵션을 추가(verbose)

## 압축 풀기
 - -x : 압축풀기
```
tar -xzf my_dir.tar.gz
```
 - 특정한 디렉토리에 압축을 풀도록 경로를 지정하고 싶다면 -C 옵션을 사용 하도록 한다. 만약 ~/my_dir_tmp 디렉토리에 풀고 싶다면 아래와 같이 한다.
```
tar -xzf my_dir.tar.gz -C ~/my_dir_tmp
```

## chmod 하위 파일과 폴더들에게 한번에 적용하기
```
chmod -R [8bit Permission] [file name or folder name]
```

