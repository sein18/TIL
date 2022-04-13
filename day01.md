# git 첫 수강후 정리

---

1.  CLI

---

- GUI와 CLI의 정의
  * GUI(Graphic User Interface) : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식
  * CLI(Command Line Interface) : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식  

- CLI를 사용하는 이유
  * GUI는 CLI에 비해 사용하기 쉽지만 단계가 많고 컴퓨터의 성능을 더 많이 소모한다.
  * CLI는 GUI로는 불가능한, 많은 세부적인 기능을 사용할 수 있다.
- 터미널 명령어
  * `touch` : 파일을 생성하는 명령어
  * `mkdir` : 새 폴더를 생성하는 명령어
  * `ls` : 현재 작업 중인 디렉토리의 폴더/ 파일 목록을 보여주는 명령어
  * `mv `: 폴더/파일을 다른 폴더 내로 이동 하거나 이름을 변경하는 명령어
  * `cd` : 현재 작업 중인 디렉토리를 변경하는 명령어
  * `rm` : 휴지통으로 넣지않고 완전 삭제하는 명령어로 조심!

---

2. Visual Studio Code를 활용한 git 버전 괸리

---

* Visual Studio Code의 터미널(git bash)을 이용하여 CLI명령어로 git버전관리를 배웠다.
* git 명령어
  * 일반 폴더 -> 로컬 저장소
    * git init
  * 버전 상태 출력
    * git status
  * Working Directory -> Staging Area
    * git add [File]
    * git add .  # 모든 파일 add
  * Staging Area -> Commits
    * git commit -m "commit message"
  * commits 목록 출력
    * git log
    * git log --oneline  # 한줄로 보기 옵션

---

3. markdown(Typora 사용)

---

# 제목

1~6단계

순서가 없는 목록

- , +, *
  순서가 있는 목록
  1.
  2.

드여쓰기 TAB
내어쓰기 SHIFT + TAB

기울기:*글자*
굵게:**글자**
최소선:~~취소선~~
코드(`)

인라인 코드: `코드`
불록코드: ```언어코드```

링크
[표시글자](링크)

이미지
![대체 텍스트](이미지 주소 링크)

인용

> 인용하고 싶은 구문

표
| 파이프와 -하이픈을 이용하여 작성 
ctrl + t로 만드는게 편하다.


원본 소스 보기 ctrl + /

구분선

---

4. github사용법

---

- vscode에서 터미널 열기 
  * ctrl + `
- <연결하기>
  * git remote add origin " 깃허브 경로"
- <연결확인>
  * git remote -v
- <오타난 경우 연결 삭제하기>
  * git remote rm origin
- <github에 변경사항 백업하기 , 올리기>
  * git push origin master