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

$ poetry init
This command will guide you through creating your pyproject.toml config.

Package name [my_workspace]:  # 你可以直接按 Enter 或輸入名稱
Version [0.1.0]:  # 你可以直接按 Enter
Description []:  # 你可以直接按 Enter
Author [None, n to skip]:  # 請直接輸入你的作者名稱 Peter <liyanglin08@gmail.com>，你可以輸入 n 來跳過這一項
License []:  # 你可以直接按 Enter
Compatible Python versions [^3.7]:  # 選擇 Python 版本或按 Enter
Would you like to define your dependencies (require) interactively? (yes/no) [yes]: no  # 如果不需要新增依賴，可以選擇 "no"
Would you like to define your development dependencies (require-dev) interactively? (yes/no) [yes]: no  # 如果不需要開發依賴，可以選擇 "no"


使用 Poetry 安裝套件

poetry add pandas numpy

啟用虛擬環境

poetry shell
