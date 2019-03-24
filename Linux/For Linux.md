## su (switch user) 명령어
- 현재 계정을 로그아웃 하지 않고 다른 계정으로 전환하는 명령어
```
su
// su [user_name], su root 사용자로 변경 -> root 암호를 임력해야 한다

su user 01
// 다른 사용자로 변경한다

su - user01
// 다른 사용자로 변경하면서 환경변수까지 적용하낟. (su, su - 차이)

whoami
// 현재 사용자를 확인한다

logout (또는 exit)
// 이전 계정으로 돌아온다

su -c 'apt-get update'
// root 권한으로 하나의 명령만 실행한다
```