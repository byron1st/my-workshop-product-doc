@Import
* all as `lo` from [1레벨 논리 뷰](https://github.com/byron1st/my-workshop-doc/blob/master/doc/arch.views.1.logical.md)

# Level 1: 모듈 뷰
## 다이어그램들
### MO01: 개발 측면 시스템 구조
![MO01](https://github.com/byron1st/my-workshop-doc/blob/master/images/module-view-mo01-2016-08-19.png)

`lo.IPC`는 Electron의 IPC 라이브러리인 `ipcRenderer`, `ipcMain`을 이용한다.

#### 추적성 매핑
* `MainWindow` (컴포넌트)
  * `lo.MainWindow`
* `App` (컴포넌트)
  * `lo.App`
* `ipcRenderer`, `ipcMain` (외부 컴포넌트)
  * `lo.IPC`

## 도출된 요소들
* 컴포넌트
  * `MainWindow`
  * `App`
