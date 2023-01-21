# Python Dictionary

## math library

### gcd(numbers)

- 최대공약수

### lcm(numbers)

- 최소공배수

## String

### stringData.replace('old String','new String')

- old String을 new String으로 변경

### stringData.split('seperator')

- seperator 기준으로 문자열을 분리하여 리스트로 반환

### seperator.join(List)

- 리스트 내 요소 사이사이에 seperator를 넣어 문자열로 반환

### stringData.lstrip(characters to delete) / rstrip / strip

- 괄호 안의 문자열들을 삭제
- lstrip: 왼쪽에서 부터 괄호 안의 문자열이 나오지 않을때 까지 제거
- rstrip: 오른쪽에서부터 괄호안의 문자열이 나오지 않을 때 까지 제거
- strip: 양 옆에서 제거

### translate

- table를 만들고 text.translate(table)
- table = text.tableName({
  'old':'new',
  'old2':'new2'
  })

### re.sub(regex, new_regex, target)
