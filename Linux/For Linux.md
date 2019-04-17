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
