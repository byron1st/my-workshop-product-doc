@Import
* {`AS01`, `AS02`, `AS04`} from [설계전략](./arch.strategies.md)
* all as `m` from 도출된 요소들 of [1레벨 모듈 뷰](./arch.views.1.module.md)

# 레벨 2: 모듈 뷰
## 다이어그램들
### MO02: `m.MainWindow` 분해
![MO02](../images/module-view-mo02-2016-08-19.png)
* 설계 근거: `AS01`, `AS02`

### MO03: `m.App` 분해
![MO03](../images/module-view-mo03-2016-09-14.png)
* 설계 근거: `AS01`, `AS02`, `AS03`

`AS02`를 적용하여 `IPC` 모듈은 `Action` 모듈에 dependency injection 기법을 이용하여 의존성을 실행 중에 추가해준다. 테스트 시에는 Electron IPC 대신 목업을 넣어 시험한다. `Util` 모듈은 시스템의 기본적인 정보를 갖고 있으므로, 필요한 모듈은 누구나 접근할 수 있도록 허용한다.
