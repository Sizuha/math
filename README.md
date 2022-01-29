# 산술

## 나머지 연산: mod와 rem의 차이
양수일 때는 문제가 없으나, 음수가 포함된 나머지 연산의 경우는 연산이 mod 혹은 rem 방식에 따라 결과가 달라진다.

### rem
원점인 0을 기준으로 나머지를 계산.
```
예:lisp> (rem -5 3)
-5 = -3 x 1 - 2
=> 나머지 -2
```
위 경우, -방향으로 5보다 작은 3의 배수가 3이되고, -3에서 -5로 가기 위해서는 -방향으로 2만큼 더 가야 하기 때문에 나머지 결과가 -2가 된다.

### mod
-방향의 무한대를 기준으로 나머지를 계산.
```
예:lisp> (mod -5 3)
-5 = -3 x 2 + 1
=> 나머지 1
```
-방향으로 5보단 큰 3의 배수를 먼저 찾으면 -6이 되고, -5는 +방향으로 1만큼 와야 하므로 나머지 결과는 1이 된다.

# 기하
## 직선
### 직선의 기울기
두 점이 주어였을 때의 기울기(m)
```
m = ( y1 - y2 ) / ( x1 - x2 )
```
### 직선 방정식
기울기가 m인 점(P)에서 거리(T) 만큼 떨어져 있는 점(Q) 구하기
```
dx = T / sqrt(1 + m*m)
dy = T * m / sqrt(1 + m*m)

Q1 = (Px + dx, Py + dy)
Q2 = (Px - dx, Py - dy)
```
