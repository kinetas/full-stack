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

