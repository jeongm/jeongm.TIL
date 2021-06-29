## [백준]14916_거스름돈(python)

```python
n = int(input())

mini_coin = n//2+1

for i in range(0,n//5+1):
    cnt = 0
    nn = n
    nn = nn-5*i
    
    if nn%2 != 0 :
        continue
    else: 
        cnt = i+nn//2
        if cnt<mini_coin:
            mini_coin = cnt

if mini_coin == n//2+1:
    print(-1)
else :
    print(mini_coin)    
```
