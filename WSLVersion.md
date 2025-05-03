使用 Poetry 管理 Python 專案（WSL 環境）完整流程筆記

一、環境準備

1. 進入 WSL（Linux 子系統）

wsl

2. 確保已安裝 Python（建議使用 pyenv 管理）

⸻

二、安裝 Poetry

1. 安裝 Poetry（使用官方安裝指令）

curl -sSL https://install.python-poetry.org | python3 -

2. 設定環境變數 PATH

export PATH="$HOME/.local/bin:$PATH"

3. 確認安裝成功

poetry --version

三、設定專案資料夾

1. 前往 Windows 的工作目錄（範例）

cd /mnt/c/Users/Tibame/Desktop/my_workspace

2. 初始化 Poetry 專案

poetry init

依照提示輸入（以下可直接 Enter 跳過）：
	•	Package name：Enter
	•	Version：Enter
	•	Description：Enter
	•	Author：可輸入 Peter <liyanglin08@gmail.com> 或 n 跳過
	•	License：Enter
	•	Compatible Python versions：Enter
	•	Define dependencies interactively? → no
	•	Define dev-dependencies interactively? → no
	•	Do you confirm generation? → yes

3. 查看 pyproject.toml

cat pyproject.toml

四、安裝專案依賴

安裝範例依賴（如 pandas, numpy）

poetry add pandas numpy

五、啟動虛擬環境

方法一：讓 Poetry 幫你啟動（推薦）

poetry shell

方法二：手動啟動虛擬環境（路徑可能依每台機器不同）

source /home/ibame/.cache/pypoetry/virtualenvs/my-workspace-fr4v0Y-n-py3.11/bin/activate

執行後，命令列會變成這樣：

(my-workspace-fr4v0Y-n-py3.11) ibame@LAPTOP:/mnt/c/Users/Tibame/Desktop/my_workspace$

六、使用虛擬環境中的 Python

執行 Python 程式（在虛擬環境中）

python your_script.py

七、額外操作指令

安裝新的依賴

poetry add 套件名稱

離開虛擬環境

deactivate

重新啟動虛擬環境

poetry shell

或（手動方式）：

source /home/ibame/.cache/pypoetry/virtualenvs/my-workspace-xxx/bin/activate