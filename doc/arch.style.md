@Import
* {QA02} from [Quality Attributes](https://github.com/byron1st/my-workshop-doc/tree/master/doc/req.qa.md)
* {AS01} from [설계전략](https://github.com/byron1st/my-workshop-doc/tree/master/doc/arch.strategies.md)

# Architecture Style
## Client-Server Style
* 근거: QA02

Electron의 `Main` 프로세스와 `Renderer` 프로세스를 Client-Server 스타일로 설계한다. `Main` 프로세스에 프로그램의 실행, 전역 메뉴 기능, Persistence 저장 기능을 할당하고 UI와 연관된 기능은 `Renderer` 프로세스에 할당함으로써 역할을 명확히 분할하여 QA02를 해결한다.
## Flux Architecture Style
* 근거: AS01

`Main` 프로세스와 `Renderer` 프로세스에 각각 Flux Architecture를 적용한다.
