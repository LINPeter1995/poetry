# poetry

curl -sSL https://install.python-poetry.org | python3 -

export PATH="$HOME/.local/bin:$PATH"

poetry --version

設定 Poetry 使用 pyenv 的 Python

poetry new my_project
cd my_project
poetry env use $(pyenv which python)

使用 Poetry 安裝套件

poetry add pandas numpy

啟用虛擬環境

poetry shell
