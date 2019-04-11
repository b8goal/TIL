## 파이썬 3에서 한글 텍스트 파일 읽기
```py
f = open('파일명','r', encoding='utf8')
text = f.read()
print(text)
```
	
## 딕셔너리 key에 value를 리스트로 update하기
```py
if key not in dictionary:
	dictionary[key] = [val]
else:
	dictionary[key].append(val)
```

## append 와 extend 함수의 차이점
```py
x = [1, 2, 3]
x.append([4,5])
print(x)

[1, 2, 3, [4,5]]
# append()는 object를 맨 뒤에 추가합니다.
```
```py
x = [1, 2, ,3]
x.extend([4, 5])
print(x)

[1, 2, 3, 4, 5]
# extend()는 iterable 객체(리스트, 튜플, 딕셔너리 등)의 엘레먼트를 list에 appending 시킨다.
```
