@Import
* all from [Functional Requirements](https://github.com/byron1st/my-workshop-doc/tree/master/doc/req.func.md)
* all from [설계전략](https://github.com/byron1st/my-workshop-doc/tree/master/doc/arch.strategies.md)

# Level 1: Scenario View
* 모든 다이어그램에서 `User`에서 시작되는 `emitEvent()`는 `User`가 직접 UI 요소를 마우스/키보드 등으로 실행시키는 것을 의미한다.
* `User`로 반환되는 `show()`는 UI가 변경되어 User가 눈으로 이를 확인함을 의미한다.

## SC01: 사용자가 메인 창의 UI를 통해 실행하는 기능 시나리오 1
![SC01](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc01-2016-08-18.png)
* 관련 기능들: UC01, UC02, UC03, UC04, UC05, UC06, UC07, UC08, UC14, UC15, UC16
* 설계 근거: AS04

사용자가 실행한 기능이 메인 앱에서 수행된다.

## SC02: 사용자가 메인 창의 UI를 통해 실행하는 기능 시나리오 2
![SC02](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc02-2016-08-18.png)
* 관련 기능들: UC12, UC13
* 설계 근거: AS04

사용자가 실행한 기능이 UI 수준에서만 수행된다.

## SC03: 사용자가 메인 메뉴를 통해 실행하는 기능 시나리오
![SC03](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc03-2016-08-18.png)
* 관련 기능들: UC09, UC10, UC11
* 설계 근거: AS04

## SC04: 프로그램이 실행될 때 시나리오
![SC04](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc04-2016-08-18.png)
* 관련 기능들: UC01, UC02, UC03, UC14, UC15
* 설계 근거: AS04

사용자가 프로그램을 실행 시켰을 때 프로그램이 초기 데이터를 불러오고 UI 등을 생성하는 시나리오이다.
