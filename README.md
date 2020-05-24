# README
This Repository is Test for Python

# 環境構築

## インデックス

1. 環境を確認する
1. Homebrew をインストールする
1. Homebrew を使い pyenv をインストールする
1. pyenv を使い Pythonをインストールする
1. Pythonのコードを実行する

## 1. 環境を確認する
Macでは標準でPythonがインストールされているので、バージョンを確認する。

```
$ python --version
```

## 2. Homebrew をインストールする

### Homebrewがインストールされているか確認する

```
$ brew -v

-> brew: command not found
```

### Homebrewがインストールされていない場合

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brew -v

-> Homebrew 2.2.17
```

## 3. Homebrew を使い pyenv をインストールする

### pyenv(パイエンブ)
複数のバージョンのPythonを管理するツール。

```
$ pyenv -v

-> pyenv: command not found

$ pyenv -v

-> pyenv 1.2.18
```

### シェルにパスを通す(zshの場合)

```
$ echo $SHELL

-> /usr/local/bin/zsh

$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
$ echo 'eval "$(pyenv init -)"' >> ~/.zshrc
$ source ~/.zshrc
```

## 4. pyenv を使い Python をインストールする

### インストールするPythonのバージョンを確認する

```
$ pyenv install --list

-> 最新安定板をインストールする
```

```
$ pyenv install 3.8.2

$ pyenv versions

-> * system (set by /Users/user_name/.pyenv/version)
-> 3.8.2
```

### インストールしたバージョンのPythonを設定する

```
$ pyenv global 3.8.2
```

### ターミナルを再起動する

```
$ python --version

-> Python 3.8.2
```

## 5. Pythonのコードを実行する

```
$ touch script.py
$ echo 'print("Hello, Python")' >> script.py
$ echo 'print(1+2)' >> script.py

$ python script.py

-> Hello, Python
-> 3
```
