# 레벨 3: 실행 뷰
## 다이어그램들
### EX01: 프로그램 런칭(launch) 될 때 각 요소 생성 구조
![EX01](https://github.com/byron1st/my-workshop-doc/blob/master/images/execution-view-ex01-2016-08-20.png)

### EX02: 프로그램 실행 시 구조
![EX02](https://github.com/byron1st/my-workshop-doc/blob/master/images/execution-view-ex02-2016-08-20.png)

### EX03: 오브젝트 전송 구조
![EX03](https://github.com/byron1st/my-workshop-doc/blob/master/images/execution-view-ex03-2016-08-20.png)

* `rel1`: DB에서 꺼낸 오브젝트를 바로 수정하면, DB와 쌍방향 동기화가 될 수 있다. 그러한 사태를 막기 위해 Immutable 객체로 변환 후 필요한 작업을 하여 전송한다.
* `rel2`: 이유는 모르겠지만, Immutable로 감싸진 오브젝트도 Electron IPC를 거치면 plain 오브젝트로 변경된다.
* `rel3`: Immutable로 감싸진 store와 일관성을 유지하기 위해 IPC로 전송받은 오브젝트를 Immutable로 감싼다. (향후 변경 가능.)
