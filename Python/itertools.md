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

## Combinatoric Iterators

### Product()

- 카테시안 곱 연산
- n개로 구성된 모든 조합 생성

```python
from itertools import product

print(list(product('ABCD',repeat = 2)))
print()
print(list(product(['AB','CD','EF'],'2',repeat = 2)))
print()
print(list(product(['AB','CD'],'2')))

print(list(product('AB',[2,1])))


```

```
		[('A', 'A'), ('A', 'B'), ('A', 'C'), ('A', 'D'), ('B', 'A'), ('B', 'B'), ('B', 'C'), ('B', 'D'), ('C', 'A'), ('C', 'B'), ('C', 'C'), ('C', 'D'), ('D', 'A'), ('D', 'B'), ('D', 'C'), ('D', 'D')]

        	[('AB', '2', 'AB', '2'), ('AB', '2', 'CD', '2'), ('CD', '2', 'AB', '2'), ('CD', '2', 'CD', '2')]

            [('AB', '2'), ('CD', '2')]


```

### permutations()

- 순열 생성

### combinations()

- 조합 생성

### combinations_with_replacement()

- 요소 중복 허용 조합 생성

## Iterators terminating on the shortest input sequence

### accmulate()

- 시퀀스의 누적 합을 구할 때 사용

```python
from itertools import accumulate

    lists = [1,3,5,7,9]
    data = accumulate(lists)
    print(*data)
```

```
1 4 9 16 25
```

### chain()

- List 연결 시 사용함

```python
from itertools import chain
    listDataNum = [2,4,6,8,10]
    listDataChar = ['A','B','C','D']

    finalData = chain(listDataNum,listDataChar)

    print(*finalData)

```

```
2 4 6 8 10 A B C D
```

### set1.intersection(set2) / set1&set2

- set1과 set2의 교집합

### set1.union(set2) / set1|set2

- set1과 set2의 합집합

### set1.difference(set2) / set1 - set2

- set1과 set2의 차집합

### set1 ^ set2

- 대칭 차집합

### set1.update([list])

- 집합 요소 추가

### set1.remove()

\*집합 요소 제거

### for 문의 두가지 형태

```python
a = [i*i for i in range(5)]
print(a)
```

```
[0,1,4,9,16,25]
```

### reversed()

- 리스트 내 항목들의 순서를 뒤집음

### map(type, LISTNAME)

- 리스트 LISTNAME을 type으로 변환

### dict

#### list -> dict

1.

n%10
n/=10

map
