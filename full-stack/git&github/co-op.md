# 협업도구
## 1.git
git은 형상관리도구이지만 협업 도구인 깃허브 연동을 위한 도구 중 하나  
1. 전역설정
  - git config --global user.email "your email"
  - git config --global user.name "your nickname"
  - git config --list

2. 기본 명령어
  - git init : Working directory생성
  - git add
  - git commit

3. 확인 명령어
  - git log
  - git log --oneline

4. 되돌리기
  - git reset --soft
  - git reset --hard
  - git option
    - hard : 돌아간 커밋 이후의 변경 이력을 전부 삭제 working directory까지 리셋을 하지만 tracked된 상태여야 함
    - soft : 변경 이력 삭제, 변경 내용은 남아있음, 인덱스 초기화(git add가 안되어 있는 상태)
    - mixed : 변경 이력 삭제, 변경 내용은 남이있음, 인덱스도 유지(git add까지 되어 있음)
  - git reflog
  - git rm --cached filename (tracked file -> untracked file)

5. branch
  - git branch : 브랜치들을 확인
  - git branch 브랜치이름 : 브랜치 생성
  - git switch 브랜치이름 : 브랜치 전환
  - git checkout 브랜치이름 : 브랜치 전환 + 여러기능

6. 병합하기
  - git merge 브랜치이름 : git switch로 병합 위치 선정 후 merge로 불러오기 (여기에 브랜치이름을 merge해라)
    - Fast-Forward : 커밋 생성x merge기본옵션
    - non-Fast-Forward : 커밋 생성o git merge 브랜치이름 --no-ff
      - --no-ff로 하면 커밋 이름을 적으라고 창이 뜸 이때 나가기 위해서는 :wq를 사용해 나갈 수 있음
      - --no-ff -m "커밋내용"으로 하면 바로 커밋됨
    - git merge --continue :충돌 후 파일을 병합처리를 위해 수정 후 git add로 스태이징한 다음 해당 명령어로 이전에 병합하다 충돌이 일어난 것을 이어서 진행
  - 언제나 병합 후 master브랜치 이외의 브랜치도 head를 맞춰줘야 함
  - merge에서 보통 main,dev,user1이 있을 때 user들의 개발 내용을 dev에 병합하고 마지막으로 main에 dev의 내용을 병합하는데 이때는 --no-ff로 하면 관리하기 좋다


## 2.github

1. 깃허브 가져오기
- git clone 깃허브에서 최초로 가지고 올 때
- git pull 깃허브에서 가지고 온 후 반영
- git fetch 깃허브에서 가지고 오기

2. 깃허브에 저장하기
- git push 깃허브에 저장

# 협업도구

---

## 1. Git

git은 형상관리도구이지만 협업 도구인 깃허브 연동을 위한 도구 중 하나

---

### 1) 전역 설정

- git config --global user.email "your email"
- git config --global user.name "your nickname"
- git config --list

---

### 2) 기본 명령어

- git init : Working directory 생성
- git add
- git commit

---

### 3) 확인 명령어

- git log
- git log --oneline

---

### 4) 되돌리기

- git reset --soft
- git reset --hard
- git option

  - hard  
    : 돌아간 커밋 이후의 변경 이력을 전부 삭제  
    : working directory까지 리셋  
    : tracked된 상태여야 함

  - soft  
    : 변경 이력 삭제  
    : 변경 내용은 남아있음  
    : 인덱스 초기화 (git add가 안되어 있는 상태)

  - mixed  
    : 변경 이력 삭제  
    : 변경 내용은 남아있음  
    : 인덱스 유지 (git add까지 되어 있음)

- git reflog
- git rm --cached filename  
  (tracked file → untracked file)

---

### 5) Branch

- git branch  
  : 브랜치 목록 확인

- git branch 브랜치이름  
  : 브랜치 생성

- git switch 브랜치이름  
  : 브랜치 전환

- git checkout 브랜치이름  
  : 브랜치 전환 + 여러 기능 포함

---

### 6) 병합하기

- git merge 브랜치이름  
  : git switch로 병합 위치 선정 후 merge 실행

---

#### 병합 방식

- Fast-Forward  
  : 커밋 생성 없음  
  : merge 기본 옵션

- non-Fast-Forward  
  : 커밋 생성 있음  
  : git merge 브랜치이름 --no-ff

  - --no-ff 사용 시 커밋 메시지 입력 창이 열림  
    종료 : :wq

  - git merge 브랜치이름 --no-ff -m "커밋내용"  
    : 바로 커밋 이름과 함께 생성

- git merge --continue  
  : 충돌 발생 후 파일 수정  
  : git add로 스테이징  
  : 병합 이어서 진행

---

#### 병합 전략

- 병합 후 main 브랜치 이외의 브랜치도 head를 맞춰야 함

- 브랜치 목록  
  - main  
  - dev  
  - user1

- user 브랜치 → dev 병합  
- dev -> main 병합  

이때 dev -> main 병합은 --no-ff 사용 시 관리에 용이함

---

## 2. GitHub

---

### 1) 깃허브 가져오기

- git clone  
  : 최초로 원격 저장소를 가져올 때

- git pull  
  : 원격 저장소에서 가져온 후 즉시 반영

- git fetch  
  : 원격 저장소에서 가져오기 (병합 없음)

---

### 2) 깃허브에 저장하기

- git push  
  : 원격 저장소에 업로드
