# ODetect

> [V1.0.0 / 2019.08.18]
1. 介面大致完成，不斷優化中
2. 登入錯誤提醒改成snakbar
3. 將主畫面切成兩個fragment載入
4. 可從手機上傳圖片並同步至cloud storage及database
5. 從database撈資料給"個人資料"(未來優化:不要每次onclick就撈一次)
6. 完成登出功能(UI還沒)
7. 新增toolbar、floating button


> [V1.0.1 / 2019.08.18]
1. 修改"個人資料"頁面
2. 新增"更換名稱"、"更換密碼"


> [V1.0.2 / 2019.08.19]
1. 重構"個人資料"排版按鈕
2. 新增"個別管理" recycle view、下拉動畫
3. 新增"農場概況"頁面

> [V1.0.3 / 2019.08.21]
1. 優化登入頁
   (字體大小、邊界差距、驗證內容、使用者體驗、取得權限時直接跳轉bug)
2. 優化"個別管理"點擊動畫
3. 使用AsyncTask抓取checkImageURL文字及圖片放入recyclerview
   (bug:還沒抓取完就載入recyclerview、動態控制陣列大小)

> [V1.1.0 / 2019.08.26]
1. 調整資料庫架構，新增溫室類別，移除checkImageURL
   (註冊時預設溫室1，可於個人資料新增溫室數量)
2. 註冊、上傳圖片預設database路徑及storage路徑更新
3. "上傳圖片"新增spinner，可動態調整上傳路徑位置
4. "個別管理"新增spinner，可動態顯示各溫室內容
5. 上傳圖片時開啟新的thread發送包含辨識URL的socket給server
   (三秒偵測server有沒有ACK，若沒有則重新request)
6. (python)辨識後的圖片已可上傳至storage並將資訊同步於database

> [V1.1.1 / 2019.08.27]
1. 修正recyclerview介面超出問題(暫時改為Linearlayout)
2. 可動態控制"個別管理"陣列大小
3. 新增登入時的Reveal動畫，修改背景顏色
4. 解決上傳圖片會閃退

> [V1.1.2 / 2019.08.28]
1. "個別管理"新增左滑刪除功能，可同步刪除database及storage資料(結果圖還沒刪)
2. 修復切換溫室時，內容是其他溫室的