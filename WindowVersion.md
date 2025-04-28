要使用 Poetry，你本機必須先安裝好 Python

看起來你在 Windows PowerShell 嘗試安裝 Python 的 Poetry 工具時，遇到了一些問題。這裡是根據你的錯誤訊息整理的分析和解決方法：

🔍 問題整理：
你已執行

powershell

(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py -
系統回應是：

The latest version (2.1.2) is already installed.

➤ 表示安裝已完成。

但你接著執行

powershell

poetry --version

系統回應：

無法辨識 'poetry' 詞彙是否為 Cmdlet...

➤ 表示 Poetry 沒有加到你的 PATH 環境變數。

你試圖使用 Linux 風格的安裝語法：

POETRY_HOME=/etc/poetry python3 -
➤ 這段語法是 Linux 或 macOS bash shell 的格式，不能直接在 PowerShell 使用。

✅ 解決方式：

📌 1. 確認 Poetry 安裝位置

Poetry 通常會安裝在使用者目錄下的 AppData\Roaming\Python\Scripts 或 .poetry\bin。請執行以下指令來找出 poetry.exe 的路徑：

Get-ChildItem -Path $env:USERPROFILE -Recurse -Filter "poetry.exe" -ErrorAction SilentlyContinue

📌 2. 手動加入 PATH
若你找到 poetry.exe 例如在這裡：

C:\Users\Tibame\AppData\Roaming\Python\Scripts\

請將這個路徑加到你的系統環境變數中。

方法：

開啟【系統環境變數】 > 【環境變數】

找到「使用者變數」中的 Path > 編輯

新增你找到的 poetry.exe 所在資料夾的路徑

儲存後重新開啟 PowerShell，再輸入：

poetry --version
