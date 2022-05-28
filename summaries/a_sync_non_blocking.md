## Sync-Blocking(동기 블로킹)

- 동기 블로킹 : A실행시 B를 호출과 동시에 B에게 제어권을 넘긴다할때, A는 제할일을 못하고 대기!

	- 추가예정

## Sync-Nonblocking(동기 논블로킹)

- 동기 논블로킹 : A실행시 B를 호출 리턴하면서 A가 자신을 실행시킬 수 있음.
- 동기 논블로킹의 예시

```
function runSync(result) {
	return result = '서버에서 온 사람입니다';
}

const cb1 = result => {
	console.log('누구세요? :', result);
};

function main() {
	const syncObj = runSync();
	cb1(syncObj);
	console.log('함수는 종료');
}

main();

// main함수에서 cb1에 할당받은 콜백함수로 넘어가지만 main은 미완료이므로 수행중임. 콜백함수 끝나며 main은 종료.
```


## Async-Nonblocking(비동기 논블로킹)

- 비동기 논블로킹 : A실행시 B를 호출과 동시에 B에게 콜백함수를 넘김. A가 제할일 하면서 B는 자신이 끝난후에 콜백을 실행시킴!
- 비동기 논블로킹의 예시

### Promise

- Promise는 다음 state(상태) 중 하나에 있습니다.
	1. pending(보류 중) : 이행도 거부도 아닌 초기 상태.
	2. fulfilled(충족) : 작업이 성공적으로 완료되었음을 의미합니다.
	3. rejected(거부됨) : 작업이 실패했음을 의미합니다.

- promise 가 종료가 되면 resolve 에 들어간 값을 then(cb1)에 받을 수 있습니다.
- PromiseState가 fulfilled되었을때, PromiseResult(실행시 받은 resolve값)를 반환해줌!

```
function runAsync(time) {
	return new Promise(resolve => {
		setTimeout(() => {
			resolve('서버에서 온 사람입니다');
		}, time);
	});
}

const cb1 = result => {
	console.log('누구세요? :', result);
	return runAsync2(3000);
};

function main() {
	const asyncObj = runAsync(1000);
	asyncObj.then(cb1).then(cb2);
	console.log('함수는 종료');
}

main();

// promise로 인한 비동기상황
```