# todoMVC 練習

## 初始化
* 切分元件，將 app 元件中的內容，分散至 `header`, `list` 和 `footer` 元件中。
* 新增服務元件 `list-service`，並利用環境變數檔，找到正確的 `api` 路徑，撰寫 [非同步請求]() 邏輯。

---
## header 元件
* `<input/>` 按下 `enter` 後，發出 `http request`，新增 todo 事項。
  * 成功，清空 input，更新 `list` 元件。
  * 失敗，input 保留，發出 alert 訊息，[新增失敗]()。

---
## list 元件
* 利用服務 `list-service` 拿到代辦資料 `task`。
* 利用列表資料渲染畫面。
  * 將 `task` 的名稱綁定至 `<li/>` 元素中的 `<label/>` 元素中。
  * 利用 `task` 的屬性 `isDone`，決定事項是否已完成，完成事項的 `<li/>` 元素 `class` 名稱，應含有 [completed]()。
* 在 `<li/>` 元素中的 `<label/>` 元素，新增 [雙擊開啟編輯]() 功能
  * 當 [編輯]() 模式啟動後，`<li/>` 元素 `class` 名稱，應含有 [editing]()。
  * [編輯]() 模式啟動後， `class` 名稱為 [edit]() 的 `<input/>` 才可出現在 `html` 結構中
  * 當使用者不再 focus 上述 `<input/>` 上或按下 `enter` 時，[解除編輯模式]()，並發出 `http request` [更新]() 該事項
  * 呈上，若使用者按下 esc 鍵，不更新事項，[解除編輯模式]()
* 在 `class` 為 [destroy]() 的 `<input/>` 上，完成刪除功能，發出 `http request` [刪除]() 該事項
* 在 `class` 為 [toggle]() 的 `<input/>` 上，完成更新 [已完成狀態]() 功能
* 在 `class` 為 [toggleAll]() 的 `<input/>` 上，完成更新全部事項 [已完成狀態]() 功能
---
## footer 元件
* 當事項數量為 [0]() 時，不顯示
* 顯示當前事項數量
  * 在 `<strong/>` 元素內，顯示已完成的事項數量
  * 在 `<strong/>` 元素後，字樣 `left` 之前，顯示 [未完成]() 的事項數量
* 在 `class` 為 `clear-completed` 的按鈕上，完成 [清除所有]() 已完成事項功能

---
## Reference 
* [json-server 文件說明](https://github.com/typicode/json-server)
* [todoMVC 功能展示](http://todomvc.com/examples/angularjs/#/)
