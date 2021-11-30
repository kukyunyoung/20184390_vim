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

![vimgolf 2_27](https://user-images.githubusercontent.com/71830573/144053931-d7b91554-ee68-442b-82d8-58654feac955.gif)

2번 문제입니다.

문제를 분석해보니 **sublime** 단어는 단한번 나오고 첫번째문장에서 2번째 단어에 등장을 했습니다.

**emacs**는 문장의 무작위의 위치에 5개가 배치되어 있었습니다.

그래서 **sublime** 단어가 7개의 키입력을 차지하니 이것을 해결하고 **emacs**는 한번에 치환하는 방법이 좋을것같다라고 생각했습니다.

W 를 입력해 **sublime** 위치에 가서 dw 입력을 통해 잘라내기를 해주었습니다. 그래서 7번의 백스페이스나 delete 키 입력대신 두번의 키입력으로 단어를 지울수 있었습니다.

그리고 i vim ESC 를 입력해 sublime의 치환을 마쳤습니다. 

emacs 를 vim 으로 치환하기 위해서 :%s/emacs/vim/g 를 입력해주었습니다.

치환을 해야하는 단어가 한개밖에 없는것과 첫번째문장의 두번째단어가 치환해야하는 단어인 점인 것을 감안하면

꼼수를 썼는데도 교수님이 제시한 해답과 키입력이 같다는 점에서 이 방법은 별로 좋지 못하다고 생각했습니다.

![vimgolf 2_27_good](https://user-images.githubusercontent.com/71830573/144056605-df6e5973-50aa-425c-85f9-cb2e4fa1c9b5.gif)

첫번째 방법은 교수님이 제시해주신 방법과 키입력이 똑같지만 좋지못한 방법이라고 생각하여 **sublime** 단어와 **emacs** 단어를 전부 **vim**단어로 치환해줬습니다.

g 옵션을 주지않으면 조금더 키입력이 줄어들지 않을까 생각하여 실행에 옮겨봤더니 **emacs** 단어 한개가 치환이 되지 않아 g옵션을 주었습니다.
