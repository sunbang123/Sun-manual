# Git 터미널 에러

- remote: Invalid username or password.
```
git remote remove origin
git remote add origin https://닉네임:토큰@github.com/repository 경로
```

- warning: [config-설정이름] has multiple values
```
git config --global --replace-all [config-설정이름] "[config-설정 value]"
```

- warning: LF will be replaced by CRLF in [file 이름]
```
$ git config --global core.autocrlf false
```
	- 에러 가능성 있으므로 업로드 후엔 다시 true로 돌려놓자!

- remote: error: this exceeds GitHub's file size limit of 100.00 MB
	- 100.00MB 크기가 넘는 파일을 업로드시 발생하는 에러입니다.

- hint: Updates were rejected because the tip of your current branch is behind ...
	- pull을 먼저 해서 로컬 저장소와 git의 상태가 동일해야 하는데 그렇지 않아서 발생한다.
```
git pull origin main --rebase
```