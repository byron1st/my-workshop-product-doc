# UI 설계
## React Component 설계
### UI Wireframes
각 상태는 아래 U01을 참조한다.
#### U03: View 상태의 Wireframe
![View 상태의 Wireframe](https://github.com/byron1st/my-workshop-doc/blob/master/images/ui-u03-2016-09-19.png)

색으로 처리된 영역은 React Component를 의미하며, 이 Component들의 계층 구조는 U02를 참조한다.

#### U04: SubView 상태의 Wireframe
![SubView 상태의 Wireframe](https://github.com/byron1st/my-workshop-doc/blob/master/images/ui-u04-2016-09-19.png)

### UI 상태 다이어그램
#### U01: UI 상태 다이어그램
![UI 상태 다이어그램](https://github.com/byron1st/my-workshop-doc/blob/master/images/ui-u01-2016-09-14.png)

A0 ~ A8은 상태 Transition들의 ID를 의미하며, [상세 설계](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.detail.md)의 Action들 정의에 사용된다. Action들은 각 상태 Transition에 매핑된다.

### React Component들
#### U02: React Component들 계층 구조
![React Component들 계층 구조](https://github.com/byron1st/my-workshop-doc/blob/master/images/ui-u02-2016-09-14.png)