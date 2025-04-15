# poetry

進入你的 WSL Linux 環境

wsl

安裝 Poetry

curl -sSL https://install.python-poetry.org | python3 -

設定 PATH

export PATH="$HOME/.local/bin:$PATH"

確認安裝成功

poetry --version

進入你的工作區資料夾(資料夾右鍵複製路徑)
在 WSL 中，Windows 的磁碟分區會被掛載到 /mnt 目錄下。例如，C: 驅動器會映射到 /mnt/c

cd /mnt/c/Users/Tibame/Desktop/my_workspace


在現有資料夾中初始化 Poetry

poetry init

使用 Poetry 安裝套件

poetry add pandas numpy

啟用虛擬環境

poetry shell
