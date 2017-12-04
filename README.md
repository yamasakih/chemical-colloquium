# chemical-colloquium 
このリポジトリは12/5に行う化学コロキウムの講義資料を収めたものです  
勉強会の開催概要などは以下のページを御覧ください  

# 事前準備について

受講者の方はこのページをよく読み、事前にハンズオン環境の準備を整えておいてください  
所要時間は1時間ほどです  

## 講義資料のダウンロードおよびハンズオン環境のインストール
ハンズオン用のJupyter NotebookやRDKitをAnacondaでインストールし、講義資料を[Jupyter](http://jupyter.org/)で閲覧できるようにします

行うことは以下の２点です。

- リポジトリのクローンもしくはダウンロード
- Anacondaのインストール

### リポジトリのクローンもしくはダウンロード
Windows環境で `git` がインストールされていない場合は以下のページから `git` をインストールしてください  
- https://git-for-windows.github.io/

任意の位置(例えばホームディレクトリなど)で実行してください  

```
git clone https://github.com/chemo-wakate/tutorial-6th.git
```

続けて

```
git clone https://github.com/yamasakih/chemical-colloquium.git
```

と２つのリポジトリをクローンしてください。

うまくできない場合は、[https://github.com/chemo-wakate/tutorial-6th.git](https://github.com/chemo-wakate/tutorial-6th.git)と  
[https://github.com/yamasakih/chemical-colloquium.git](https://github.com/yamasakih/chemical-colloquium.git)をダウンロードしておいてください

### Anacondaのインストール
[Anaconda](https://www.anaconda.com/download/)を使用することでハンズオンに必要な Jupyter notebook や rdkit を使用することが可能です

#### Windowsの場合
お使いのパソコンが32bitあるいは64bitかでダウンロードするものが変わるので注意してください。

##### 32bit
上記のサイトからAnaconda (Python version2.7) をダウンロードし、インストールしてください  
インストール中の  

- Add Anaconda to my PATH environment variable, 
- Register Anaconda as my default Python 2.7

という項目どちらにもチェックを入れてください

##### 64bit
上記のサイトからAnaconda (Python version3.6) をダウンロードし、インストールしてください  
インストール中の  

- Add Anaconda to my PATH environment variable, 
- Register Anaconda as my default Python 3.6

という項目どちらにもチェックを入れてください

##### モジュールのインストール
続けて追加で必要なモジュールをインストールします。

スタートメニューからAnaconda→Anaconda Promptを起動します
(少し起動に時間がかかると思います)

起動したら以下のように実行します  
(パソコンの性能によっては長いと30分ぐらいかかります)

```
conda install -y -c rdkit rdkit
```

処理がすべて終了したら続けて以下のように実行します

```
conda install -y numpy==1.13.1
```

インストールが完了したら作業終了です。

#### Macの場合
##### Homebrewのインストール
まずHomebrewをインストールします  
Homebrewはこちらのサイトの指示に従ってインストールできます  
[Homebrew macOS 用パッケージマネージャー](https://brew.sh/index_ja.html)

ターミナルを起動して以下のように実行するとHomebrewがインストールされます。

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

##### pyenvのインストール
続けてHomebrewを利用してAnacondaをインストールに必要なpyenvをインストールします

```
brew install pyenv
```

インストールが終わったらpyenvへパスを通すために以下のコマンドを打ち込みます

```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
source ~/.bash_profile
```

##### Anacondaのインストール
続けてAnacondaをインストールします

```
pyenv install anaconda3-4.1.1
```

と入力するとAnacondaがインストールされます

続けて

```
pyenv global anaconda3-4.1.1
```

と入力しデフォルトの起動をインストールしたanaconda3-4.1.1にします。

##### モジュールのインストール
最後に必要なモジュールをインストールします  
以下のように実行します  
(パソコンの性能によっては長いと30分ぐらいかかります)

```
conda install -y -c rdkit rdkit
```

処理がすべて終了したら続けて以下のように実行します

```
conda install -y numpy==1.13.1
```

インストールが完了したら作業終了です。
