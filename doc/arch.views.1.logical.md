@Import
* all as `sc` from [1레벨 시나리오 뷰](https://github.com/byron1st/my-workshop-doc/tree/master/doc/arch.views.1.scenario.md)
* {`AS04`} from [설계전략](https://github.com/byron1st/my-workshop-doc/tree/master/doc/arch.strategies.md)

# Level 1: 논리 뷰
## 다이어그램들
### LO01: 실행 측면 시스템 구조
![LO01](https://github.com/byron1st/my-workshop-doc/blob/master/images/logical-view-lo01-2016-08-18.png)
* 설계 근거: `AS04`

#### 추적성 매핑
* `MainWindow` (컴포넌트)
  * `sc.MainWindow`
  * `sc.updateUI()`
* `App` (컴포넌트)
  * `sc.App`
  * `sc.reqFunc()`
  * `sc.init()`
  * `sc.appFunc()`
* `IPC` (커넥터)
  * `sc.request()`
  * `sc.getInitData()`
  * `sc.refreshUI()`

## 도출된 요소들
* 컴포넌트
  * `MainWindow`
  * `App`
* 커넥터
  * `IPC`
