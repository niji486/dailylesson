# 생활강의요약(Pull Request)

> code review(release전 개발자간 검증단계)의 기능으로서 pull/merge request 

- 2가지 케이스 존재 
  - 원격조정소(repository)에 Write으로 접근가능한 경우
  - 원격조정소에 Write불가능하나 오픈 소스여서, 다른 원격조정소로 카피 후(fork) push하는경우
    --> 작업 후 본래 원격조정소에 나의 코드를 검토해봐주세요라는 요청이 pull request
- branch에 대한 정책 셋팅이 중요함
  - master 는 원본과 최종본의 역할로 정의하고 개발작업은 별도 브랜치로 하는 것으로 rule 
    - 보통 features 라고 함. 
- push 하고 난 이후에 pull request 를 할 수 있도록 link를 자동 생성함. 
  - command 후 나오는 설명에서 pull request link 를 확인 
  - github에서 commit 마다 있는 link 활용 
  - 혹은 commit 에서 pull request link 요청 
- Pull request --> merge request
  - 보통은 merge 요청으로 하면서 메시지 작성 
  - reviewer : 품평할 수 있는 사람, assignees : 실제 작업을 해줄 수 있는 사람 
  - draft pull request : 작업이 미완료전으로 검토는 할 수 있으나 merge는 되지 않음 
  - e-mail 발송으로 pull request 를 전송함 
  - conversation : 여러 사건을 시간순서대로 보여줌 
  - commit : 이 branch 에서 생겨난 commit 을 알려줌
  - files change : 최종적인 working directory 의 상태 
  - 검토 후 만족스러우면 Merge request 
- code review 
  - add single review : 등록 후 바로 comment 가 보여짐 
  - start review : 부분 review를 먼저 남긴 후 전체 finish 후 남긴 모든 리뷰가 보여짐. 
- 충돌 해결하기 
  - pull request를 해두면 실시간으로 conflict 감시를 하기 때문에, 오류 발견이 쉽다.  
- 개념비교
  - merge pull request : feature를 없애고 master로 모두 병합하는 작업
  - squash and merge : feature의 복사버전으로 만들어 master에 업데이트하는 방법
    feature 는 남지만, master 에 그동안의 버전관리 기록이 남지 않음
  - rebase and merge : feature의 각 단계별 버전으로 master 에 붙여 feature도 남기고, 버전기록도 남기는 방법 
  - 협업을 위해 프로젝트의 과정으로 최대한 심플하게 하는 것이 중요

