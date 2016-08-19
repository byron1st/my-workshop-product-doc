# 레벨 3: 코드 뷰
## 모듈 뷰와 추적성 표현
[추적성 테이블](https://www.icloud.com/numbers/0Er5f_DK9yL8iv9R2YEq6UEDA#trace-module-code)

## `mainwindow/flux/store.js`의 데이터 구조 설계
```
{
	itemType: string,
	mainList: array,
	subList: array,
	modalList: array,
	mainListEdit: bool,
	itemEdit: bool,
	modalEdit: bool,
	selected: object,
	modalSelected: object
}
```

## LokiJS의 DB 구조 설계
![DB](https://github.com/byron1st/my-workshop-doc/blob/master/images/code-view-db-2016-08-19.png)
