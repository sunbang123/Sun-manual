## Git 초기 설정

1. 다음 링크를 통해 github의 access token을 발급받는다.
	- https://curryyou.tistory.com/344
2. git-bash를 우클릭 관리자 권한으로 실행 후 다음 명령어를 입력
	a. git config --local --unset credential.helper
	b. git config --global --unset credential.helper
	c. git config --system --unset credential.helper
	d. git config --global user.name "본인이름"
	e. git config --global user.email "본인 이메일 주소"
	f. git pull
	g. username 입력하라고 팝업 창이 뜸 (github에서 your profiles 페이지의 주소 창에 있는 username을 입력)
	h. password는 1번에서 발급 받은 토큰 입력
3. 다음 명령어로 비밀번호 저장을 한다.
	- git config credential.helper store
