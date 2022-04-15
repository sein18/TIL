# git 2일차 수강 후 정리

---

1. git clone, pull

---

* clone
  - 원격 저장소의 커밋 내역을 모두 가져와 로컬 저장소에 생성하는 명령어
  - clone `복제`라는 뜻으로, git clone (URL)을 통해 복제 한다.
  - git clone을 통해 복제된 로컬 저장는 `git init`, `git remote add` 가 포함 되어있다.

```bash
$ git clone <https://~~/~.git>
```

- pull

  - clone과는 다르게 원격 저장소를 통해 변경사항을 가져와서, 로컬 저장소를 업데이트하는 명령어
  - 로컬 저장소와 원격 저장소의 내용이 완전 일치하면 `git pull`을 하더라도 변화가 일어나지 않는다.

  ```bash
  git pull origin master(branch)
  ```

  

---

2. .gitignore

---

* gitignore
  - git을 이용하여 원격 저장소(github)에 버전 관리를 하는 과정에서 숨겨야하는 키 또는 코드를 숨기도록 지정하는 것이다.
  - `.gitignore` 파일을 `.git` 폴더와 동일한 위치에 생성한 후 제외하고 싶은 파일의 이름을 저장한다.
  - `java`,`python`,`c++` 등을 숨기기 위해서는 [gitignore.io](https://gitignore.io/) 사이트를 이용하면 편리하다.

---

3. branch설명 용어

---

* branch

  -  Branch는 `나뭇가지`라는 뜻의 영어 단어다.
  -  즉 `브랜치`란 나뭇가지처럼 여러 갈래로 작업 공간을 나누어 **독립적으로 작업**할 수 있도록 도와주는 Git의 도구다.

* git branch (조회, 생성, 삭제 명령어)

  * 브랜치 `조회, 생성, 삭제 등` 브랜치와 관련된 Git 명령어

    ```bash
    # 브랜치 목록 확인
    $ git branch
    
    # 원격 저장소의 브랜치 목록 확인
    $ git branch -r
    
    # 새로운 브랜치 생성
    $ git branch <브랜치 이름>
    
    # 특정 커밋 기준으로 브랜치 생성
    $ git branch <브랜치 이름> <커밋 ID>
    
    # 특정 브랜치 삭제
    $ git branch -d <브랜치 이름> # 병합된 브랜치만 삭제 가능
    $ git branch -D <브랜치 이름> # (주의) 강제 삭제 (병합되지 않은 브랜치도 삭제 가능)
    ```

* git switch(이동, 이동과 동시에 브랜치생성)

  * 현재 브랜치에서 다른 브랜치로 `HEAD`를 이동시키는 명령어 `HEAD`란 현재 브랜치를 가리키는 포인터를 의미합니다.

    ```bash
    # 다른 브랜치로 이동
    $ git switch <다른 브랜치 이름>
    
    # 브랜치를 새로 생성과 동시에 이동
    $ git switch -c <브랜치 이름>
    
    # 특정 커밋 기준으로 브랜치 생성과 동시에 이동
    $ git switch -c <브랜치 이름> <커밋 ID>
    ```

---

4. Beanch Merge(합병)

---

* branch merge

  * 현재까지는 독립된 작업 공간을 만드는 법만 진행했으며 협업을 통해 합치는 방법이다.
  * `git merge <합칠 브랜치 이름>` 의 형태로 사용한다.
  * merge를 하기전에 메인 브랜치로 설정하여 사용한다.

  ```bash
  # 1. 현재 branch1과 branch2가 있고, HEAD가 가리키는 곳은 branch1 입니다.
  $ git branch
  * branch1
    branch2
  
  # 2. branch2를 branch1에 합치려면?
  $ git merge branch2
  
  # 3. branch1을 branch2에 합치려면?
  $ git switch branch2
  $ git merge branch1
  ```

* `git branch -d <합친 후 메인브랜치말고 남음 브랜치> ` 제거 해준다.(메모리 관리 차원)

