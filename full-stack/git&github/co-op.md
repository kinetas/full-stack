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
    - merge기본 옵션
    - Fast-Forward : 커밋 생성x
    - non-Fast-Forward : 커밋 생성o
  - 


## 2.github
