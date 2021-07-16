# 생활코딩 강의 요약

### (1) git CLI back up

-  확실하지만 번거로운 방법 : 물리적으로 떨어져있는 backup  서버를 설치하여 본 PC 와 back up PC가 네트워크를 통해 교신하도록 함. 아무나 접속하지 못하도록 보안작업을 겹겹히 하도록 함. 
- 제한적이지만 쉬운 방법 : 인터넷에 연결된 PC는 host.  host를 서버로 임대해주는 hosting. git 서비스를 제공하는 hosting, git hosting. 

### (2)  용어 정리

- 지역저장소 local repository : 작업하는 본 PC
- 원격저장소 remote repository 
- PUSH : 지역저장소 --> 원격저장소로 보내 같은 상태로유지, back up
- CLONE : 원격저장소와 다른 장소의 지역저장소를 복제화하는 것
- PULL : 원격저장소 --> 지역저장소로 같은 상태 유지 

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

- git remote add [별명] [원격저장소주소]
- git hosting 에서 제공하는 https 기준 보여지는 원격저장소 링크 복사 
- 기본적인 원격저장소는 origin  으로 별명
- git remote, git remote -v 는 연결된 원격저장소 정보 보기 

### (7) git push

- git push --set -upstream origin master
- github에서 업로드된 파일과 commit log 확인 