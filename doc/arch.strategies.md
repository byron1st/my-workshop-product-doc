@Import
* {QA01, QA02} from [Quality Attributes](https://github.com/byron1st/my-workshop-doc/tree/master/doc/req.qa.md)

# 설계전략
## AS01: Flux Architecture Style 적용
* 근거: QA01, QA02

Flux Architecture의 단일화된 Dispatcher-Action 구조는 데이터를 변경시키는 기능을 Action 파일 내에 집중시키므로 QA02를 해결한다.

Store, Dispatcher, Action, React Component가 느슨하게 연결된 구조 덕분에 Store, Dispatcher, Action을 모두 독립적으로 테스트 할 수 있어 QA01을 해결한다.

## AS02: Electron API 분리
* 근거: QA01

Electron은 실행 시 라이브러리를 로드하기 때문에, Electron 앱을 실행시키기 않는 단위 테스트에서는 의존성 에러를 유발시킨다. 그렇기 때문에 Electron API는 아키텍처 컴포넌트의 포트(Port)로 설계하고, 단위 테스트는 수행하지 않는다.

만약, 의존성 에러를 피할 수 없을 경우 [`Electron-Mocha`](https://github.com/jprichardson/electron-mocha) 사용을 고려한다. 다만, 이 경우 `sendSync` 함수에 의해 프로그램이 무한히 대기하는 상황에 빠지지 않도록 주의한다.

## AS03: 테스트 모드 분리
* 근거: QA01

UI가 제대로 자리 잡혀있는지를 보기 위해, 개발 중 Electron 앱을 실행 시킬 때는 테스트 모드로 작동한다. 테스트 모드에 실행될 경우, 미리 정의된 세이브 파일에서 데이터를 로드한다. 테스트 모드 여부를 저장하고 있는 설정 파일은 빌드의 자동화를 위해 JSON 파일로 저장하며, 다른 설정 파일과는 분리시킨다.

## AS04: Client-Server Architecture Style 적용
* 근거: QA02

Electron의 `Main` 프로세스와 `Renderer` 프로세스를 Client-Server 스타일로 설계한다. `Main` 프로세스에 프로그램의 실행, 전역 메뉴 기능, Persistence 저장 기능을 할당하고 UI와 연관된 기능은 `Renderer` 프로세스에 할당함으로써 역할을 명확히 분할하여 QA02를 해결한다.
