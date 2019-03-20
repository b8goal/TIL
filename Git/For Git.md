## 깃 리모트 변경 하기

### 기존 리포지토리 깔끔하게 pull / push
```
git pull
git add .
git commit -m "clean push"
git push
```

### 기존 리포지토리 remote 제거
```
git remote remove origin
```

### 새 리포지토리 remote 추가
```
git remote add origin https://github.com/playauto/리포지토리명 
```

### Git add 취소하기 (파일 상태를 Unstage로 변경하기)
- 아래와 같이 실수로 git add * 명령을 사용해 모든 파일을 staging Area에 넣은경우
- Staging Area(git add 명령 수행한 후의 상태)에 넣은 파일을 빼고 싶을 때

```
// 모든 파일이 Staged 상태로 바뀐다.
git add *
// 파일들의 상태를 확인한다.
git status
```

- 이때, git reset HEAD [file] 명령어를 통해 git add를 취소할 수 있다.
- 뒤에 파일명이 없으면 add한파일 전체를 취소한다.
- CONTRIBUTING.md 파일을 Unstaged 상태로 변경해보자.

```
// CONTRIBUTING.md 파일을 Unstaged로 변경한다.
git reset HEAD CONTRIBUTING.md
// 파일들의 상태를 확인한다.
git status
```

### 끝 