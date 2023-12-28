# python 문법, 활용

### 2023-12-27(수)
***
- 정렬된 순서를 유지하면서 배열 a에 x를 삽입할때 가장 왼쪽 or 오른쪽 인덱스를 반환
```
from bisect import bisect_left, bisect_right

print(bisect_left(a,x))  
print(bisect_right(a,x))
```

### 2023-12-29(금)
***
from itertools import combinations

lst = ['A', 'B', 'C']
print(list(map(''.join, itertools.combinations(lst, 2))))

