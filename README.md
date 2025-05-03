Poetry 安裝問題與解決方案（Windows PowerShell）

你使用 PowerShell 安裝 Poetry：

(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py -

系統顯示：

The latest version (2.1.2) is already installed.

表示 Poetry 已安裝完成。

但執行：

poetry --version

poetry 不是內部或外部命令...

表示系統找不到 poetry 指令，原因是 未將 Poetry 安裝路徑加入 PATH 環境變數。

解決方式

步驟 1：找出 Poetry 安裝路徑

請執行以下 PowerShell 指令尋找 poetry.exe 所在位置：

Get-ChildItem -Path $env:USERPROFILE -Recurse -Filter "poetry.exe" -ErrorAction SilentlyContinue

常見路徑可能是：

C:\Users\你的使用者名稱\AppData\Roaming\Python\Scripts\

或

C:\Users\你的使用者名稱\AppData\Roaming\Python\Poetry\bin\

步驟 2：將路徑加入環境變數 Path

開啟 系統環境變數設定：

在搜尋欄輸入「環境變數」並開啟 「編輯系統環境變數」。

點擊右下角【環境變數 (Environment Variables)】

在「使用者變數」找到 Path，點【編輯】

點【新增】，將剛才找到的 Poetry 路徑貼上

儲存所有視窗並關閉

步驟 3：重新啟動 PowerShell

關閉目前的 PowerShell 視窗，再開啟新的，輸入：

poetry --version

若成功，會顯示類似：

Poetry (version 2.1.2)
