# Code Peer Review Templete

- 코더 :  박기용, 김진홍
- 리뷰어 : 차정은

---

# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.

- [ ] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [x] 주석을 보고 작성자의 코드가 이해되었나요?
- [x] 코드가 에러를 유발할 가능성이 있나요?
- [ ] 코드 작성자가 코드를 제대로 이해하고 작성했나요? (직접 인터뷰해보기)
- [ ] 코드가 간결한가요?

---

# 예시

1. 코드의 작동 방식을 주석으로 기록합니다.

2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.

3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.

```python
maze = [[0, 1, 0, 0, 0], [0, 0, 0, 1, 0], [0, 1, 1, 0, 0], [0, 0, 1, 1, 0], [0, 0, 0, 0, 0]]




# start_x = maze[0][0]
# start_y = maze[0][0]

i=start_x = 0
j=start_y = 0
           
                                      # 2차원 리스트의 값을 바꿔 줄 수 있는 함수 정의
def solve_maze(*args):              
  for i in range(5):
    for j in range(5):         # 4,4까지 도달해야 하는 함수 정의, 가는 도중 1이 있으면 print
      if maze[i][j] == 0: # 현재 좌표에서 1에 닿으면 이동해줘야 함
        goto(40)
        maze[i][j] = 2
        print("미로를 찾을 수 없습니다.")
      elif maze[i][j] != 0 :
        if maze[i+1][j] == 0:
          right(90)
          maze[i+1][j] = 2
        print("미로를 찾았습니다.")
                                # 지나갈 수 있는 길, 리스트 내부 값을 2로 변경해줘야 함 

## review comment
## solve_maze 함수의 매개변수는 x, y좌표로 고정되어있기 때문에 가변인수로 받지 않았어도 될 것 같습니다
## 현재 위치에서 상하좌우로 1칸씩만 움직일 수 있기 때문에 이중 반복문으로 해결하기에는 어려운 문제가 아니었나 생각합니다. 상하좌우 좌표를 조건문으로 길인지(0) 아닌지(1)를 확인하는 방식으로 구현하셨으면 좋을 것 같습니다:)

goto(start_x, start_y)
solve_maze(start_x, start_y)
import pprint
pprint.pprint(maze)
# 행을 한 칸씩 오른쪽으로 이동하다가 1을 만나면 밑으로 가고나서 오른쪽으로, 밑에서 1을 만나면 위로 가고 오른쪽으로 가는 함수, 끝까지 가면 아래쪽으로 이동
```

---

# 참고 링크 및 코드 개선 여부

파이썬 거북이 미로 게임(https://blog.naver.com/PostView.nhn?blogId=ytlee64&logNo=222104805578&parentCategoryNo=&categoryNo=37&viewDate=&isShowPopularPosts=true&from=search)
