@Import
* all as `f` from [Functional Requirements](https://github.com/byron1st/my-workshop-doc/blob/master/doc/req.func.md)
* {`AS01`, `AS02`, `AS04`} from [설계전략](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.strategies.md)
* {`SC01`, `SC02`, `SC03`, `SC04`} from [1레벨 시나리오 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.scenario.md)
* all as `sc` from 도출된 요소들 of [1레벨 시나리오 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.scenario.md)

# 2레벨: 시나리오 뷰
## 공통 사항
* 모든 다이어그램에서 `User`에서 시작되는 `emitEvent()`는 `User`가 직접 UI 요소를 마우스/키보드 등으로 실행시키는 것을 의미한다.
* `User`로 반환되는 `show()`는 UI가 변경되어 User가 눈으로 이를 확인함을 의미한다.
* UML 2.1의 Sequence diagram을 따른다.

## 다이어그램들
### SC05: DB request
![SC05](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc05-2016-08-19.png)
* 설계 근거: `AS04`, `AS02`

IPC를 통해 들어오는 DB 요청(CRUD)은 IPC에서 DB로 바로 이어지도록 한다. IPC와 DB는 분리한다.

### SC06: Dispatch an Action
![SC06](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc06-2016-08-19.png)
* 설계 근거: `AS01`

Flux Architecture 구조를 반영한다.

### SC07: Dispatch an IPC action
![SC07](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc07-2016-08-19.png)
* 설계 근거: `AS01`, `AS02`

IPC를 Flux Architecture 요소들에서 분리한다.

### SC08: Update UI
![SC08](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc08-2016-08-19.png)
* 설계 근거: `AS01`, `AS02`

UI는 [React 라이브러리](https://facebook.github.io/react/)를 선정한다. React 라이브러리는 Flux Architecture와 조합이 가장 잘 맞는 UI 컴포넌트이다. 또한 `AS02`에 따라, IPC를 호출하는 Action은 분리한다.

### SC09: Initialize
![SC09](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc09-2016-08-19.png)
* 설계 근거: `AS03`

테스트 모드 여부를 프로그램 실행 가장 초기(DB 로딩 전)에 검사한다.

### SC10: Revised `SC01`
![SC10](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc10-2016-08-19.png)

### SC11: Revised `SC02`
![SC11](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc11-2016-08-19.png)

### SC12: Revised `SC03`
![SC12](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc12-2016-08-19.png)

### SC13: Revised `SC04`
![SC13](https://github.com/byron1st/my-workshop-doc/blob/master/images/scenario-view-sc13-2016-08-19.png)

## 도출된 요소들
* 컴포넌트
  * `sc.App`
    * `IPC`
    * `DB`
    * `Main`
    * `AppMode`
    * `Settings`
    * `MainMenu`
    * `Dispatcher`
    * `Action`
  * `sc.MainWindow`
    * `Dispatcher`
    * `Store`
    * `Action`
    * `IPC`
    * `React UI components`
* 커넥터 (생략)

## 레벨 1 설계로부터의 추적성
* `sc.App`
  * `IPC`
  * `DB`
  * `Main`
  * `AppMode`
  * `Settings`
  * `MainMenu`
  * `Dispatcher`
  * `Action`
* `sc.MainWindow`
  * `Dispatcher`
  * `Store`
  * `Action`
  * `IPC`
  * `React UI components`
* `sc.request()`
  * `request()`
* `sc.reqFunc()`
  * `SC05`
* `sc.updateUI()`
  * `SC08`
* `sc.appFunc()`
  * `SC12`
* `sc.refreshUI()`
  * `refreshUI()`
* `init()`
  * `SC09`
* `getInitData()`
  * `SC08`: `actionType = IPC`
