Poetry 安裝問題與解決方案（Windows PowerShell）

你使用 PowerShell 安裝 Poetry：

(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -

步驟 1：加入環境變數-系統變數-Path

請執行以下 PowerShell 指令尋找 poetry.exe 所在位置：

Get-Command poetry

步驟 2：將路徑加入環境變數 Path

常見路徑可能是：

C:\Users\User\AppData\Roaming\Python\Scripts\

步驟 3：重新啟動 PowerShell

關閉目前的 PowerShell 視窗，再開啟新的，輸入：

poetry --version

若成功，會顯示類似：

Poetry (version 2.1.2)
