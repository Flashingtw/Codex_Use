# 第三題：BMI 體質指數計算

成品：[BMI_Exercise3.aia](BMI_Exercise3.aia)。這是獨立的 MIT App Inventor 2 專案，只包含第三題，不需先匯入第一題或第二題。

## 下載及匯入

1. 在 GitHub 開啟 `deliverables/BMI_Exercise3.aia`，按 **Download raw file** 下載。
2. 前往 https://ai2.appinventor.mit.edu/ ，選擇「專案 → 從我的電腦匯入專案（.aia）」。
3. 用 AI Companion 連線測試，或從「建置」產生 APK。

## 功能與題目標準

- 選擇男生或女生，輸入身高（公分）與體重（公斤），按「計算 BMI」。
- BMI = 體重 ÷（身高 / 100）²。
- 男生：BMI < 20 為過輕，20 ≤ BMI ≤ 25 為正常，BMI > 25 為過重。
- 女生：BMI < 18 為過輕，18 ≤ BMI ≤ 22 為正常，BMI > 22 為過重。
- 結果以文字顯示至小數第一位，並用中文語音播報。語音需裝置具備可用的中文 TTS 語音。
- 依性別及結果，顯示上傳 ZIP 中對應的六張原始 PNG 圖片；圖片內容未修改，僅使用內部英文檔名。
- 初始選擇男生，計算前不顯示圖片；切換性別會清除上一筆結果圖片。已依使用者要求移除兩張 initial 圖片及所有引用。
- 所有文字元件（標籤、核取方塊、輸入框、按鈕及對話框）的 TextColor 均依使用者要求設為 AI2「無」（`&H00FFFFFF`）。「無」是透明色，文字可能因此看不見。
- 空白、非數字、零及負數輸入會顯示提醒，避免除以零或輸入錯誤。

## 素材對應

| 上傳圖片 | 專案內部檔名 |
| --- | --- |
| Boy_Low.png | male_thin.png |
| Boy_Normal.png | male_normal.png |
| Boy_OverWeight.png | male_heavy.png |
| Girl_Low.png | female_thin.png |
| Girl_Normal.png | female_normal.png |
| Girl_OverWeight.png | female_heavy.png |

## 驗證範圍

- 137 項積木邏輯模擬斷言通過，涵蓋男女判定邊界、一位小數顯示與語音參數、錯誤輸入及性別切換。
- 使用 App Inventor 官方原始碼儲存庫中的 Blockly XML 讀取器，搭配最小元件定義，成功載入 135 個積木、3 個事件及 3 個全域變數，無解析警告。已避免先前積木命名空間前綴造成的載入問題。
- 封裝完整性、所有圖片參照及六張上傳圖片的逐位元組一致性已確認。
- 尚未在完整 AI2 網站匯入、編譯或手機上實際執行。

已驗證封裝內僅保留六張使用者提供的結果圖、沒有 initial 檔案或引用，並確認 12 個文字元件的 TextColor 均為「無」。尚未在 AI Companion 上實際測試顯示。
