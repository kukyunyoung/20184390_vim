# 오픈소스SW개론
## vimeditor vimgolf 과제



### 1. Add quotes to ansible playbook

![vimgolf 1_10](https://user-images.githubusercontent.com/71830573/144048836-9ae3cd12-e431-4031-9c8a-9c4bf3e6a8d4.gif)

1번 문제입니다.

교수님이 강의에서 해설해주신 방법 말고 다른방법으로 풀어보고자 했습니다.

**/{** 입력을 통해 **{** 위치로 바로 이동을 하고자 했습니다.

그러나 이 명령어는 2개의 입력이 필요해 교수님이 설명해주신 GW 입력을 통해 이동을 하는것과 같은수의 입력을 해야했고

**/{** 입력 후에 엔터를 치지 않고 **i**를 눌러 입력을 하고자하면 맨앞에서 입력을 시작하기때문에 결국에는 10번의 타이핑을 해야했습니다.

![vimgolf 1_9](https://user-images.githubusercontent.com/71830573/144050386-1ae73011-c85b-4d40-bf3b-6e7139d73f5c.gif)

그 후에 수차례 시도를 해봤지만 10번 미만으로 횟수를 줄일수가 없었고 결국은 교수님이 설명해주신 방법으로 문제를 풀었습니다.

G,W,i,",END,",ESC,Z,Z 순서로 입력을하여 총 9번의 입력을 통해 문제를 해결했습니다.

### 2. simple replacements
