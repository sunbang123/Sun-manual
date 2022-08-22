# Git branch

새로운 branch를 github에 등록하는 방법
1. git branch [new branch name]
2. git branch checkout [new branch name]
3. git add [new file name]
4. git push origin [new branch name]

pull request
1. github 원격 저장소에 들어간다면, pull request를 요청하는 버튼이 보인다.
2. 이를 눌러 pull request를 보낸다.

branch pull request merge
1. pull request를 전송한 branch는 main branch와 합칠 수 있는데 이를 merge라고 한다.
2. pull request처럼 merge를 요청하는 버튼을 클릭하여 main branch에 새로운 branch의 내용을 덮어씌워준다.

branch-to-branch merge
1. git checkout main // main[default] branch로 이동한다.
2. git merge [합치려는 branch 이름] // 합치려는 branch의 내용을 main branch에 복사, 합쳐줍니다.
3. git push --set-upstream origin main // main branch에 병합한 내용을 push 합니다.

branch delete
1. git checkout main // 우선 삭제하려는 branch에서 벗어난다.
2. git branch -d [삭제하려는 branch 이름]
3. git pull