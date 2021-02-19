2021.02.15

### for~else 문

파이썬에서는 else문을 for문과 같이 쓸 수 있다.   
for문과 같은 레벨에 else를 둬 for문에서 break가 실행되지 않았을 경우 else문이 실행된다.   
즉, for~else문에서 else는 for문에서 break의 실행 유무를 판단할 수 있다.   

```
a = ['딸기','바나나','수박','귤','참외','멜론','자몽']

fruit = input('무슨 과일을 먹고싶니? : ')
for i in range(len(a)):
    if a[i] == fruit:
        print(f'{fruit} 여기있어~')
        break
else:
    print(f'{fruit}는 없단다')
    
```
