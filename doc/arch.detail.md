# 상세 설계
## Behavior Model
### B02: 프로그램 실행
![프로그램 실행](https://github.com/byron1st/my-workshop-doc/blob/master/images/details-b02-2016-09-03.png)

## 함수들 정의
### Action들 정의
[Action들 정의](https://www.icloud.com/numbers/03hMQehmK-jVBH7SfOZEUZnQw#actions)

### IPC 정의
[IPC 정의](https://www.icloud.com/numbers/0lI96VlolhAmutnLItrVn8TLg#ipc)

### DB 함수들 정의
[DB 함수들 정의](https://www.icloud.com/numbers/0z6cmqVq8wW6H0fN9STF3q0ag#dbFunc)

## `mainwindow/flux/store.js`의 데이터 구조 설계
```
{
	itemType: string,
	mainList: array,
	subList: array,
	modalList: array,
	mainListEdit: bool,
	itemEdit: bool,
	modalEdit: bool,
	selected: object,
	modalSelected: object
}
```
