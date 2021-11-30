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

### 3. Satisfy the go linter

![vimgolf 3_43](https://user-images.githubusercontent.com/71830573/144063208-d9e17f97-bc40-418a-8895-9598a1034afd.gif)

입력을 최소화하기 위해 중복되는 입력인 **Version**을 복사하기 위해 /ve(3)로 **version** 단어의 앞으로 갔습니다. 그후 yw(5)를 통해 단어를 복사했습니다.

**Version string**문장 위에 주석문을 입력하기위해 k i // space esc p i space T O D O esc(19) 를 입력했습니다.

그후 **Debug**를 복사하기위해 /d(21)로 **Debug**단어의 앞으로 이동했고 yw(23)를 통해 단어를 복사했습니다.

**Debug bool**문장위에 주석을 달기위해 똑같이 k i // space esc p i space T O D O esc (41)를 입력했습니다.

마지막으로 ZZ(43)를 입력해 저장을 해주었더니 총 43번의 키입력이 나오게 되었습니다.

![vimgolf 3_43 visual](https://user-images.githubusercontent.com/71830573/144069066-38b74334-d411-4b6e-a20d-8eb0ae3dd3b2.gif)

주석을 달때 스페이스의 입력이 낭비가 되는것같아 비주얼모드로 띄어쓰기까지 복사를 해서 시도를 해보았습니다.

**Version**을 먼저 복사하기위해 /ve v w y(6)를 입력하여 **Version s**까지 복사를 해주었습니다.

그 후 주석문을 입력하기위해 i enter uppercase // space esc p R T O D O esc (21)를 입력했습니다.

**Debug**도 똑같이 복사하기 위해 /d v w y(26)를 입력하여 **Debug b**까지 복사를 해줬습니다.

이것도 똑같이 i enter uppercase // space esc p R T O D O esc(41)를 입력해 주석문을 달아주었습니다.

그리고 ZZ(43)를 입력해 총 43번의 키입력을 하게 되었습니다.

결국 같은 횟수의 키입력이 나와서 더 좋은 결과는 못얻게되었습니다.

### 4. Plotting some variables in python

[vimgolf 4_67](https://user-images.githubusercontent.com/71830573/144086476-d3050dd9-5ace-42b1-8d8d-b8b50a70ac96.gif)

이 문제는 제일먼저 문자를 바꾸자고 생각했습니다. 값을 바꿔야할때 모든경우에 /를 이용해서 찾아갔는데

x1의 값을 x4로 바꾸고나서 /k로 찾아가도 첫번째행으로 이동을 하여서 이동의 낭비가 있었습니다. 그래서 문자를 먼저 바꾸자고 생각했습니다.

문자를 바꿀때 i를 이용하면 지우고 입력을 해야하므로 낭비가 있기때문에 R을 이용해 최소한의 입력으로 문자를 바꾸었습니다.

그 후 :%s/y1/abs(y1)/g 를 이용해 y1에 abs를 씌워줬습니다.

/x 를 이용해 x값으로 찾아갔는데 4번째 행부터 시작을 했습니다.

Ctrl+a 를 이용하면 i 나 R의 이용없이 숫자의 값을 올릴 수 있었습니다.

4번째행을 A를 입력해 3번올려주고 위로올라가 2번올려주고 위로올라가 1번올려주었더니 x는 모두 바꿨습니다.

같은방법으로 #과 y의 숫자값도 모두 바꿔주었습니다.


### 5. Python dataclasses!


![vimgolf 5_46](https://user-images.githubusercontent.com/71830573/144077465-0b9ab727-80eb-4cf6-babe-6c4d8e4e586c.gif)

모든 단어를 한개씩 복사해서 "" 안에 넣어주려고 했습니다.

"" 를 찾아갈때 /" 를 통해 찾아가니 처음 큰따옴표 뒤에서 시작을 하여서 맨뒤의 요소부터 넣어주려고 했습니다.

먼저 **score**를 찾아갔는데 /sc를 입력해 찾아가보았습니다. 그후 yw(5)를 입력해 복사를 해주었고 /" enter p로 큰따옴표 사이에 복사를 해주었습니다.

그다음 **age**를 찾아갔습니다. /ag enter yw로 **age**를 복사해주었고, /" enter p a , esc로 **score**앞에 요소를 넣어줬습니다.

**name**은 중간라인에 있었기때문에 /로 찾기보다는 M을 통해 바로 위치를 찾을 수 있었습니다.

M yw /" enter p a , esc로 조금더 적은 입력으로 찾을 수 있었습니다.

**student_id**을 /로 찾기위해서 /st를 입력하면 ```class Student:```와 겹쳐서 입력의 낭비가 있었습니다.

그래서 M k 를 통해 위치를 찾아주었습니다.

M k yw /" enter p a , esc로 요소삽입을 끝내고 ZZ로 마무리를 해줘서 총 46번의 키입력이 나오게 되었습니다.

이방법으로 문제를 풀고 제출한 gif를 가만히 보고있다보니 /로 단어를 찾는건 enter를 무조건 입력해야해서 비효율적이라는 생각이 들었습니다.

그래서 복사해야하는 단어의 수가 4개이고 가운데문장 기준 위에2개 아래1개이다보니 M 명령어를 활용하면 더 적은 키입력을 할 수 있을것이란 생각을 했습니다.

![vimgolf 5_43](https://user-images.githubusercontent.com/71830573/144081683-342cdcc6-b933-4935-a8a4-2a347a9e4094.gif)

처음부터 그냥 M j j 를 통해 **score**을 찾았습니다. /sc enter 대비 한개의 입력이 줄어든셈입니다.

똑같이 yw를 통해 복사를 하고 /" enter p를 해주어 삽입을 했습니다.

**age** 또한 M j 로 찾았습니다. 기존 /ag enter 대비 두개의 입력이 줄어들었습니다.

yw /" enter p a , esc 로 삽입해줬습니다.

**name**은 원래 M으로 찾았기에 변화가 없고 **student_id** 또한 마찬가지입니다.

그래서 총 3번의 입력을 절약하여 43번의 결과를 얻을 수 있었습니다.
