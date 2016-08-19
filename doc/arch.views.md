# Architecture Views
## 설계 절차
설계 절차는 시나리오 뷰 설계부터 시작한다. 시나리오 뷰는 주요 기능들의 실행 모습을 가장 추상적인 수준에서 표현한다. 그 후 시나리오 뷰를 통해 도출된 요소들을 기반으로 실행 측면의 시스템 구조를 표현하는 논리 뷰를 설계한다. 그리고 이를 개발 측면(또는 코드 측면)의 시스템 구조를 표현하는 모듈 뷰로 매핑한다. 논리 뷰와 모듈 뷰가 충분히 분해 되었다고 판단되었을 때, 모듈 뷰의 요소들을 기반으로 코드 뷰를 설계한다.
## 설계
1. 1레벨 설계
  1. [시나리오 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.scenario.md)
  2. [논리 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.logical.md)
  3. [모듈 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.module.md)
2. 2레벨 설계
  1. [시나리오 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.2.scenario.md)
  2. [논리 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.2.logical.md)
  3. [모듈 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.2.module.md)
3. 3레벨 설계
  1. 모듈 뷰
  2. 실행 뷰
  3. 코드 뷰
