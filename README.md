# python 문법, 활용

### 

- 정렬된 순서를 유지하면서 배열 a에 x를 삽입할때 가장 왼쪽 or 오른쪽 인덱스를 반환
  
```
from bisect import bisect_left, bisect_right

a = [1,2,3,3,5,6,7]
x= 3

print(bisect_left(a,x))  # 2
print(bisect_right(a,x)) # 4

```

###
- 리스트중에 조합을 전부다 알려줌( 순서 상관 X, 즉 AB와 BA를 같이봄)
- EX) [1,2,3]  = > [12] [13] [23]
```
from itertools import permutations  # 중복포함
from itertools import combinations  # 중복없음

array= [1,2,3]
for i in combinations(array, 2):
    print(i)  #(1,2)(1,3)(2,3)

////////////////////////////////////

# 재귀로 구현해보기
def comb(arr,n)
  result = []
  if n == 0:
    return [[]]
  for i in range(len(arr)):
    elem = arr[i]
    for rest in range(arr[i+1:],n-1)
#   for rest in range( arr[:i] + arr[i+1:], n-1) <== 순열일때 
      result.append([elem]+ rest)
  retrun result

```


- 반시계 방향으로 돌기
  
```
for i in ((dr+3)%4,(dr+2)%4,(dr+1)%4,dr)

```




- 소수 찾기 
  
```
        if n <2:          # 2보다 작으면 소수x
            continue
        check = True
        for i in range(2,int(n**0.5)+1): 
            if n % i == 0:    # 하나라도 나눠떨어지면 소수x
-결론은 이 두개다 해당이 안되야 소수임
```

- 2차원 리스트에서 index찾기 
  
```
for i, row in enumerate(arr):
    for j, col in enumerate(row):
       if col == "찾고자 하는 값":
           print(i,j)
```
