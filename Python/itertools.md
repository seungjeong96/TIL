# itertools

- 파이썬의 내장 라이브러리

## iterator

- 다음에 들어올 값을 순서대로 리턴할 수 있는 객체
- next method를 이용해 다음 값을 불러올 수 있음

## Infinite Iterators

### count(start,[step])

- start 부터 step 만큼 증가하는 무한히 수열을 생성
- range와 다르게 숫자의 limit이 없음 -> break가 필요함

Example

```python
from itertools import count

for i in count(10,15):
    if i<=100:
        print(i)
    else:
        break
```

```
10
25
40
55
70
85
100
```

### repeat(value, [number])

- 넘겨받은 value를 number 수 만큼 반복하며 출력
- number가 제시되지 않을 경우 무한히 반복하며 출력

Example

```python
from itertools import repeat

print(list(repeat(16,8)))
```

```
[16, 16, 16, 16, 16, 16, 16, 16]
```

### cycle(iterable 객체)

- 넘겨받은 container의 요소들을 반복하며 생성
- str, list, dict, tuple 등과 같은 객체 모두 사용 가능
- 모든 요소들을 전부 돌았다면 처음으로 다시 돌아감

Example 1

```python
from itertools import cycle

for i in cycle('ALEX'):
    if i<=10:
        print(i,end=" ")
        i += 1
    else:
        break
```

```
A L E X A L E X A L
```

Example 2

```python
from itertools import cycle

testList = ["Hope","You", "Have","a", "Great","Day"]
iterators = cycle(testList)

    for i in range(15):
        print(next(iterators), end = " / ")
```

```
Hope / You / Have / a / Great / Day / Hope / You / Have / a / Great / Day / Hope / You / Have /
```

##
