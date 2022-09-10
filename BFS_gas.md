# BFS_시작점이 여러개

---

#### 시작점이 여러개인 BFS

- 시작점이 여러개인 BFS탐색의 대표적으로 가스가 퍼지는 상황이 있다.

- 이 경우, 배열에 대해 완전 탐색을 하고, visited에 넣어 주는 값을 조금만 바꿔 주면 된다.

---



#### 코드

```python
def bfs(N, M):          # 여러개의 시작점을 갖는 bfs, 시작점에서의 거리를 탐색하며 알아냄
    for i in range(N):
        for j in range(M):
            if tomato[i][j] == 1:
                Q.append((i, j))

    while Q:
        i, j = Q.popleft()
        for di, dj in [[0, 1], [1, 0], [-1, 0], [0, -1]]:
            nr, nc = i + di, j + dj
            if 0 <= nr < N and 0 <= nc < M:
                if tomato[nr][nc] == 0 and visited[nr][nc] == 0:
                    Q.append((nr, nc))
                    visited[nr][nc] = visited[i][j] + 1
```


