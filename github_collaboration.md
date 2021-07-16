# 생활코딩 강의 요약

### (1) git CLI back up

-  확실하지만 번거로운 방법 : 물리적으로 떨어져있는 backup  서버를 설치하여 본 PC 와 back up PC가 네트워크를 통해 교신하도록 함. 아무나 접속하지 못하도록 보안작업을 겹겹히 하도록 함. 
- 제한적이지만 쉬운 방법 : 인터넷에 연결된 PC는 host.  host를 서버로 임대해주는 hosting. git 서비스를 제공하는 hosting, git hosting. 

### (2)  용어 정리

- 지역저장소 `local repository` : 작업하는 본 PC
- 원격저장소 `remote repository` 
- `PUSH` : 지역저장소 --> 원격저장소로 보내 같은 상태로유지, back up
- `CLONE` : 원격저장소와 다른 장소의 지역저장소를 복제화하는 것
- `PULL` : 원격저장소 --> 지역저장소로 같은 상태 유지 

###  (3) git hosting

- 여러 서비스가 있는데 가장 유명한 것이 Github ( MS에 8조원에 인수됨 )
- Framework is open-source? 오픈소스이면 직접 PC에 설치할 수 있음, 아니면 호스팅으로만 가능 
- Open-source repostiories 에 대해서는 많은 git hosting 이 과금을 하지 않음
- Free private repositories 비공개 저장소에 대한 과금여부 

### (4) 저장소 생성

### (5) 공부의 방향

| 통신방법                                | local-->Remote | Remote-->Local |
| --------------------------------------- | -------------- | -------------- |
| HTTP(보안부족, 불편, 배울필요 없음)     | O              | O              |
| SSH(보안강력, 편리, 하지만 배우기 어렵) | X              | X              |

### (6) 원격저장소와 연결

- `git remote add [별명] [원격저장소주소]`
- git hosting 에서 제공하는 https 기준 보여지는 원격저장소 링크 복사 
- 기본적인 원격저장소는 origin  으로 별명
- `git remote`, `git remote -v` 는 연결된 원격저장소 정보 보기 

### (7) git push

- `git push --set -upstream origin master`
- github에서 업로드된 파일과 commit log 확인 

### (8) git clone

- 여러개의 저장소에 같은 파일의 상태를 유지할 수 있음
- 이동하면서 작업하는데 훌륭한 기능임. 
- github : 해당 저장소에 code >> clone >> https  주소 복사

<img src="C:\Users\joann\OneDrive\Desktop\Temporary\clone.jpg" alt="clone" style="zoom:50%;" />

- git clone [원격저장소주소] 	`[원하는디렉토리명](생략가능)	`
- ls -a 를 통해 확인

### (9) git pull

- 로컬저장소에서 업데이트 --> `push to github` --> 또다른 로컬저장소에서 `pull` 하면 완료 
- 작업할 때는 언제나 pull --> 작업 --> commit --> push 

### (10) git과 오픈소스 

- git 홈페이지 >> 소스코드 다운로드 받기 >> github 
- 다운로드 받는 방법 (1) 압축된 파일 다운로드 (2)git clone - 로컬저장소에 저장됨 

### (11) 수업을 마치며

- git 모든 저장소가 소스코드 뿐만 아니라 버전에 대한 모든 정보를 100% 복구할 수 있는 장점
- 블록체인과 같은 로직 
- push할 때마다 로그인 정보를 요청받을 때는? SSH 이용 
- issue tracker : 프로젝트를 실행할 때 마다 생기는 issue를 게시하는 곳, 협업기능과 issue tracker 활용
- 협업을 할 수 있는 만반의 준비가 끝났음. 각자의 지역저장소에 push, pull 하면서 작업 가능 
- 버전 관리를 잘하는 사람이 프로젝트 내에서 가장 중요한 사람이 될 수 있음. 
- 같은 부분을 동시에 수정하는 것 (conflict) --> 협업파트에서 conflict을 방지하는 방법을 배울것. 

### Others

- 로컬이미지를 typora에 입력 후  github에 올릴 때 : https://donggod.tistory.com/139
- github 개인토큰 : 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



