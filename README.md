# poetry

進入你的 WSL Linux 環境

wsl

安裝 Poetry

curl -sSL https://install.python-poetry.org | python3 -

設定 PATH

export PATH="$HOME/.local/bin:$PATH"

確認安裝成功

poetry --version

進入你的工作區資料夾(資料夾右鍵複製路徑) 在 WSL 中，Windows 的磁碟分區會被掛載到 /mnt 目錄下。例如，C: 驅動器會映射到 /mnt/c

cd /mnt/c/Users/Tibame/Desktop/my_workspace

在現有資料夾中初始化 Poetry

poetry init

This command will guide you through creating your pyproject.toml config.

Package name [my_workspace]:  # 你可以直接按 Enter 或輸入名稱

Version [0.1.0]:  # 你可以直接按 Enter

Description []:  # 你可以直接按 Enter

Author [None, n to skip]:  # 請直接輸入你的作者名稱 Peter <liyanglin08@gmail.com>，你可以輸入 n 來跳過這一項

License []:  # 你可以直接按 Enter

Compatible Python versions [>=3.11]:  # 選擇 Python 版本或按 Enter

Would you like to define your dependencies (require) interactively? (yes/no) [yes]: no  # 如果不需要新增依賴，可以選擇 "no"

Would you like to define your development dependencies (require-dev) interactively? (yes/no) [yes]: no  # 如果不需要開發依賴，可以選擇 "no"

Do you confirm generation? (yes/no) "yes"

查看 pyproject.toml 文件

cat pyproject.toml

安裝依賴

poetry add pandas numpy

使用 poetry env activate

poetry env activate

執行一個 source 命令來啟動虛擬環境，這樣你就可以在這個虛擬環境中運行 Python 程式

source /home/ibame/.cache/pypoetry/virtualenvs/my-workspace-fr4v0Y-n-py3.11/bin/activate

執行後，你的命令行提示符通常會變更，顯示虛擬環境的名稱

(my-workspace-fr4v0Y-n-py3.11) ibame@LAPTOP-E6T9QUMT:/mnt/c/Users/Tibame/Desktop/my_workspace$

環境隔離
這意味著在這個虛擬環境中，你可以安裝和使用專案所需的 Python 套件，並且不會影響到全系統的 Python 環境。

所有安裝的依賴（例如：pandas、numpy 等）都只會在這個專案的虛擬環境內有效。

-----------------------------------------------------------------------------------------------------------

使用專案的 Python 和依賴

python XXX.py

安裝依賴

poetry add xxx

退出虛擬環境

deactivate

激活虛擬環境

poetry env activate

source /home/ibame/.cache/pypoetry/virtualenvs/my-workspace-fr4v0Y-n-py3.11/bin/activate
