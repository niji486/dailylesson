# Branch & Conflict

### (1) 커버페이지

- branch (가지) : master -> customized directory 으로 clone 됨.
  하지만 공통 내용이 있는 경우 업무 혼란을 최소화하기 위함. 
  같은 뿌리에서 나왔지만 서로다른 버전화되가는 버전들을 관리하는 방법 
- conflict(충돌) : 같은 파일끼리 각 저장소에서 다른 내용으로 변경되어 업데이트시 충돌 발생  

### (2) 실습준비

- 3개의 work가 반영된 디렉토리 생성 

### (3) branch의 사용법

- 우리의 매뉴얼이 새로운 고객사를 만나서 고객사별로 버전을 만들어야 할 때. 
- git log --all(모두) --graph(시각화-어느 뿌리에서 나왔는지 방향을 알려줌) --oneline(간단히)
- branch 목록보기 : git branch 
- branch 생성 : git branch [신규브랜치명] 
- branch 전환 : bit checkout [전환하는브랜치명]
- 특정 업데이트 상태에서 브랜치를 늘리면, 그 이후부처 브랜치별로 버전을 기억하고 있음.
- 그야말로 가지치기에서 가져온 개념

### (4) branch 병합(Merge) 

- 어려워서 반복필요 https://opentutorials.org/course/3840/23682

- 공통의 조상인 base에서 분사된 각 브랜치의 업데이트를 합치려고 할 때 merge
- 시작하기 전! 병합 후 남기려는 branch 로 전환(checkout) 되어있는 상태여야함.
- git merge [흡수시키려는 브랜치] 
  - 파일이 다른 branch끼리 병합할 때 - branch 내 모든 파일 존재함. 
  - 같은 파일명인데 위치가 다른 곳에서 각각 변경된 branch끼리 병합할 때 - 해당 파일 내 각 브랜치에서 변경된 모든 내용을 반영하고 있음. 
  - 두가지 상황 모두 같음
- 충돌 : 같은 파일명인데 같은 위치에서 내용이 각 브랜치에서 다르게 업데이트되었을 때.
  - 병합된 파일을 보면, 구분자(<<<<<<HEAD, =====, >>>>>>)로 확인하여 수정 
  - git add [작업파일]
  - git commit
- (번외) git reset --hard [리셋하고싶은버전키]

### (5) 3 way merge

- 충돌이 일어나는 경우 

1. 브랜치끼리 병합할 때
2. 협업을 할 때

| here | base | there | 2 way merge | 3 way merge |
| ---- | ---- | ----- | ----------- | ----------- |
| A    | A    | A     | A           | A           |
| H    | B    | B     | ?           | H           |
| C    | C    | T     | ?           | T           |
| H    | D    | T     | ?           | ?           |

- 2  way conflict 보다 3 way merge 가 자동화로 풀기 훨씬 좋은 구조임
  - 3개의 브랜치 중에 1개만 변화했다면 그쪽으로 따르도록 자동화함. 
  - 2개의 경우에는 어느 쪽이 변화한 것인지 몰라서 사람이 풀어줘야 함. 

### (6) 외부 도구를 이용해서 병합하는 방법 

- p4Merge : 파일간의 차이점+병합
  - git config --global(전역) merge.tool p4mergetool
  - cat ~/.gitconfig 
  - config 란 어떤 역할인가....(추가 해결해야 할 과제)

### (7) 수업을 마치며

- 브랜치는 버릴 수 있는 작업을 만들 수 있는 최선의 도구임.  
- git workflow : git을 협업하는 모범사례를 찾아볼 것
- cherry-pick : 다른 branch 의 가장 좋은 버전만 가져와서 부분적으로 병합하는 것 
- rebase : merge 효과를 내면서도 타임라인 관리를 훨씬 더 명확하게 할 수 있음. 
- 인생에도 브랜치가 있어서, 연습 후 merge할 수 있으면 얼마나 좋을까. 



