# Python Template

Python プロジェクトを最速で立ち上げるためのテンプレートです

## 事前準備

1. pyenv インストール(Pythonバージョン管理)
1. poetry インストール(Pythonライブラリ依存管理)
1. VS Code の拡張機能をインストール


## pyenv

複数の Python バージョンを管理する

### pyenv のインストール方法

```
git clone --depth=1 https://github.com/yyuu/pyenv ~/.pyenv
export PATH="$PATH:$HOME/.pyenv/bin/"
```

※ https://github.com/pyenv/pyenv#getting-pyenv も参照

### pyenv による Python のインストール

※Python インストールはそこそこ時間がかかる

.python-version があるディレクトリで次のコマンドでインストールできる

```
pyenv install
```

次のように直接指定もできる

```
pyenv install 3.10.12
```

### pyenv 自体のアップデート

```
git -C $(pyenv root) pull origin
```

## poetry のインストール

POETRY_VERSION でバージョン固定をしておいたほうがいい。

```
curl -sSL https://install.python-poetry.org | POETRY_VERSION=1.2.0 python3 -
```

### poetry によるライブラリの追加方法

```
poetry add requests
```

#### 既存の依存ライブラリを更新せずにライブラリを追加したいとき

* pyproject.toml に 新しい依存を手動で追加
* `poetry lock --no-update` 実行
* `poetry install` 実行

## Formatter と Linter

Formatter は black と isort がおすすめ。


## VS Code の拡張機能をインストール

```
名前: Python
ID: ms-python.python
説明: IntelliSense (Pylance), Linting, Debugging (multi-threaded, remote), Jupyter Notebooks, code formatting, refactoring, unit tests, and more.
バージョン: 2023.12.0
パブリッシャー: Microsoft
VS Marketplace リンク: https://marketplace.visualstudio.com/items?itemName=ms-python.python
```


## 参考資料

* https://mirumi.tech/python-linter-and-formatter/
