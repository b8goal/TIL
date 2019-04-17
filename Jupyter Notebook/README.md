## jupyter notebook 테마 꾸미기
```
pip instsall jupyterthemes
```

### Jupyter Themes 모듈은 아래의 테마를 지원합니다. 그리고 아래와 같이 명령어를 입력할 경우 간편하게 테마를 변경할 수 있습니다. 물론 폰트도 변경할 수 있으니 조금 더 읽어주세요.
- chesterish
- grade3
- gruvboxd
- gruvboxl
- monokai
- oceans16
- onedork
- solarizedd
- solarizedl
```
jt -l # 사용 가능한 테마 목록을 출력
jt -t chesterish # chesterish 테마로 변경합니다.
```

#### 코마의 개인적인 취향을 말씀드리자면 roboto 폰트와 글자 크기 12pt 그리고 각 셀의 너비가 전체 화면의 80% 정도입니다. 요구사항에 맞추어 보니 대충 아래와 같이 명령 옵션이 설정되네요. 한번 설정하면 지속적으로 유지가 되며 default 테마로 변경하고자 하시는 분들은 jt -r 명령을 입력하시면 됩니다.
```
jt -t grade3 -f roboto -fs 12 -altp -tfs 12 -nfs 12 -cellw 80% -T -N
```