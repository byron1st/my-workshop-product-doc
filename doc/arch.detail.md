# 상세 설계
## Behavior Model
### B01: 기능 실행
![기능 실행](https://github.com/byron1st/my-workshop-doc/blob/master/images/details-b01-2016-09-03.png)
MainWindow의 UI를 통한 (버튼 등) 실행 설계이다. Action Name, IPC Name, DB function Name은 아래 '함수들 정의' 항목에서 확인할 수 있다.

### B02: 프로그램 실행
![프로그램 실행](https://github.com/byron1st/my-workshop-doc/blob/master/images/details-b02-2016-09-13.png)
프로그램이 처음 실행될 때의 실행 설계이다.

## 함수들 정의
### Action들 정의
[Action들 정의](https://www.icloud.com/numbers/03hMQehmK-jVBH7SfOZEUZnQw#actions)
상태 Transition 열은 [UI 설계](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.ui.md)의 상태 다이어그램의 상태 Transition을 의미한다.

### IPC 정의
[IPC 정의](https://www.icloud.com/numbers/0lI96VlolhAmutnLItrVn8TLg#ipc)

### DB 함수들 정의
[DB 함수들 정의](https://www.icloud.com/numbers/0z6cmqVq8wW6H0fN9STF3q0ag#dbFunc)

## `mainwindow/flux/store.js`의 데이터 구조 설계
[Store 구조 정의](https://www.icloud.com/numbers/0NBqQIbu3GQ713QQ-Tpdcde4A#store)