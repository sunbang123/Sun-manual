# 깃허브 저장소 업로드

1. 클론 된 로컬저장소에 새로운 파일을 올린다.
2. git status 를 입력하여 빨간 폰트 색상의 파일이 있는가 확인한다.
3. git add . 혹은 git add [new file] 을 통해 스테이징 한다. (업로드 준비)
	- 이때, [new file]은 내가 업로드 하고자 하는 파일 명!
	- git add . 을 하면 내가 올린 전체 파일이 스테이징된다.
	- git reset . 을 하면 내가 올린 전체 파일이 스테이징 해제 된다.
4. git commit -m "커밋 메세지를 입력하세요." 를 통해 커밋 메세지를 적는다.
5. git push
- '-f'나 '--force'는 쓰지 말도록!

### 실수로 올린 파일을 삭제하고 싶을 때

1. 로컬 저장소에 지우고 싶은 파일을 삭제한다.
2. git status를 확인하여 삭제된 파일이 빨간 폰트 색상으로 있나 확인한다.
3. git rm -r [detele file] 을 통해 삭제된 파일을 스테이징 한다.
	- 이때, git restore [detele file] 하면 삭제된 파일이 복구되므로 구분합시다.
4. git commit -m "커밋 메세지를 입력하세요." 를 통해 커밋 메세지를 적는다.
5. git push

### push한 commit message 바꾸고 싶을 때

- 강제 push를 할 수 있지만 추천하지 않습니다.
#### 처음부터 브랜치 분리를 하자!

- 그 브랜치에 해당하는 feature 개발 완료하고 (개발하는 동안은 마음대로 커밋 메시지 작성)
- main 브랜치 혹은 (develop)브랜치에 squash merge 하기.
	- squash merger: 지금까지 커밋한 내용을 하나로 뭉쳐서 커밋하는 방법
### rebase
- 기점을 변환시켜주는 코드
- 동시작업시 쓰인다.