# 깃허브 저장소 업로드

1. 클론 된 로컬저장소에 새로운 파일을 올린다.
2. git status 를 입력하여 빨간 폰트 색상의 파일이 있는가 확인한다.
3. git add . 혹은 git add [new file] 을 통해 스테이징 한다. (업로드 준비)
	- 이때, [new file]은 내가 업로드 하고자 하는 파일 명!
	- git add . 을 하면 내가 올린 전체 파일이 스테이징된다.
	- git reset . 을 하면 내가 올린 전체 파일이 스테이징 해제 된다.
4. git commit -m "커밋 메세지를 입력하세요." 를 통해 커밋 메세지를 적는다.
5. git push

### 실수로 올린 파일을 삭제하고 싶을 때

1. 로컬 저장소에 지우고 싶은 파일을 삭제한다.
2. git status를 확인하여 삭제된 파일이 빨간 폰트 색상으로 있나 확인한다.
3. git rm -r [detele file] 을 통해 삭제된 파일을 스테이징 한다.
	- 이때, git restore [detele file] 하면 삭제된 파일이 복구되므로 구분합시다.
4. git commit -m "커밋 메세지를 입력하세요." 를 통해 커밋 메세지를 적는다.
5. git push

### 최근에 push한 commit message 바꾸고 싶을 때

1. git rebase -i HEAD~n // n에는 숫자 입력
2. git commit --amend -m "바꿀 메시지"
3. git push -f origin master // 강제 push 추천하진 않음. 어쩔수 없을때 사용!