## 파이썬 3에서 한글 텍스트 파일 읽기
```
f = open('파일명','r', encoding='utf8')
text = f.read()
print(text)
```
	
## 딕셔너리 key에 value를 리스트로 update하기
```
if key not in dictionary:
	dictionary[key] = [val]
else:
	dictionary[key].append(val)
```