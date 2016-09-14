# 레벨 3: 코드 뷰
도출된 코드 요소들에 관해서는 [상위 문서](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.md)의 추적성 문서 참고

## NeDB의 DB 구조 설계
![DB](https://github.com/byron1st/my-workshop-doc/blob/master/images/code-view-db-2016-09-14.png)

Join은 DB function 수준에서 직접 구현한다. 이로 인해 성능 감소가 발생할 수 있다. 하지만 데이터 업데이트 시 데이터 사이의 일관성을 쉽게 유지할 수 있기에 이를 채택한다.

## 코딩 규칙
* [ESLint](http://eslint.org)의 기본 규칙들을 따른다.
