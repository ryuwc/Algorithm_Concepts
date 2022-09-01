# stack

### stack의 특성

- 물건을 쌓아 올리듯 자료를 쌓아 올린 형태의 구조이다.

- 저장된 자료는 1대1의 선형관계를 갖는다.

- 마지막에 삽입한 자료를 가장 먼저 꺼낸다. (후입선출)

- python에서는 list에 stack을 만든다.

- stack에 마지막 삽입한 자료의 위치를 top이라 부른다.

- push와 pop을 이용하여 자료를 삽입, 삭제한다.

<img title="" src="https://user-images.githubusercontent.com/13075035/72049492-62471c00-3302-11ea-961f-9aea3b5d98df.png" alt="push_pop" data-align="left">

### 참고 코드

```python
stack = [0]*10
top = -1
for i in range(10):
    top += 1
    stack[top] = i
print(stack)    # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

***

### 주의할 점

- 삽입할 때 에는 stack이 다 차있는지 확인해야 한다.

- 삭제할 때 에는 stack이 비어있는지 확인해야 한다. (비어있을 때 삭제하려하면, index오류난다.)

- 근데, 사실 top를 안쓰는게 편하다... 

- queue를 다룰 때와 달리 제일 뒤에 값을 삽입하고 삭제하기 때문에 그렇게 비효율적이지는 않다.

---

### 활용 예

- stack의 특성(후입선출)을 활용해, 괄호 검사에 사용될 수 있다.

<img src="https://blog.kakaocdn.net/dn/H2OrC/btqARhN2YdR/RKlHWTKtk8S7klf25Ktd80/img.png" title="" alt="check" width="573">

- 또한, 다양한 알고리즘에 활용이 가능하다.

- 다른 활용 예는 문제를 풀다가 발견하면 작성하도록 하겠다.

- stack을 활용하여 DFS, BFS에 활용 할 수 있다. (DFS, BFS는 다른 파일에서 작성하겠다.)


