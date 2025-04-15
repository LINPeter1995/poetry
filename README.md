# poetry

進入你的 WSL Linux 環境

wsl

安裝 Poetry

curl -sSL https://install.python-poetry.org | python3 -

設定 PATH

export PATH="$HOME/.local/bin:$PATH"

確認安裝成功

poetry --version

進入你的工作區資料夾

cd /path/to/my_workspace

在現有資料夾中初始化 Poetry

poetry init

使用 Poetry 安裝套件

poetry add pandas numpy

啟用虛擬環境

poetry shell
