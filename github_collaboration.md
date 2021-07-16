# 생활코딩 강의 요약(협업)

### (1) 수업소개

- git은 여러개의 저장소를 연결시켜 상호간의 동기화를 할 수 있음 ==> 협업의 도구 
- 내부적으로는  branch 가 사용되므로, branch를 알고 충돌시 해결할 수 있다면 협업을 다룰 수 있음

### (3) 같이 작업하기

- github에서 먼저 협업자 지정 
  - settings >> collaboration&teams >> collaborators 에 e-mail 추가 
  - 초대된 사람에게 e-mail 전달됨 >> accept invitation 혹은 invite link 보내기 
  - write : 개발자 권한에 해당 

### (4) push & pull 

- 동시에 작업을 하게 된 경우 git push했을 때 git 이 reject 함--> 충돌
  - 다른 사람이 작업해서 commit 한 것을 자신의 local 로 아직 업데이트하지 않았을 경우. 
  - 충돌난 부분을 수정 후 add, commit, push 진행 
  - 이 후 협업자들이 꼭 pull 을 해야함. 
- 최대한 작업을 빨리 끝내고, 자주 push를 해야하고, 시작 전 꼭 pull 하는 습관을 들여야 함. 

### (5) pull & fetch 그리고 원격 브랜치 

- git pull = git fetch -> git merge FETCH_HEAD --> commit --> push 
- .git/FETCH_HEAD : 가장 최근에 fetch 했던 내용을 merge 해줌 
- 좀더 신중하게 git 의 데이터를 pull 하고 싶을 때, 결합을 나중에 하고 fetch 로 먼저 상황 판단하기 위함. 

### (6) 수업을 마치며

- code review : Gerrit 개발자들의 코드 품질을 상호 검증하는 프로그램. 발행 전 동료들에게 검증받음 
- 어떻게 우리팀에 git을 도입할 것인가?
  - 개발진전이 있을수록 파일의 이름을 더럽혀 왔던 그동안의 작업을 상기시킨다.
  - 각자에게 익숙한 프로그램으로 빗대어 천천히 적응할 수 있도록 설명을 도운다. 