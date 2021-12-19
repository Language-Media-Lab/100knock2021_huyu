# 言語処理100本ノック 2021年度 冬
言語メディア研2021年度新入生向け勉強会として、言語処理100本ノックに取り組みます。  
教材URL: https://nlp100.github.io/ja/  

参加学生(B3)
- 岡田さん
- 橋本さん
- 矢野さん

TA(チューター)
- TBA

~~毎週全員1章分（10問）解いてください。(※ただし2章は除く)~~  
~~勉強会のときに毎週1人1章分、自分のコードを説明してもらいます。~~  
~~9章10章など，内容の難易度によって，2周間に1章になることもあります．~~  
**↑勉強会はどのように進めるのかについては現在，話し合い中です．確定後，後日発表します**  
**↑前回は上記の流れでした**  
現在，前回のような課題型にするか，それとも当日解くシステムにするのかなどについて話し合っています

## 勉強会の流れ
### B3がやること
B3がやることをここに記載する．

### TA(チューター)がやること
TA(チューター)がやること(役割)をここに記載する．


## Jupyter Notebookのテンプレート
Google colab等のJupyter Notebook形式で作成される方は以下のリンクに3章から10章までの問題文のみを記載したテンプレートを置きました．  
8章9章の問題文の数式とかをマークダウン記法で書き写すのが面倒な方はお使いください．  
https://drive.google.com/drive/folders/1vuE6o-nGLmzFAjhs25RTbTLxkgrk6D5L?usp=sharing


# Githubについて
基本的にGithubを用いて， ソースコードの管理を行います．  
Githubの使い方がわからない方は以下のサイトがおすすめです．  
https://prog-8.com/courses/git  
このサイトでは1時間ほどで， Gitの基本的な概念を理解することができます．  
チュートリアルを始める前に， 一度目を通しておいてください．  

**2021/09/28追記**  
githubがhttpsでのcloneは許可しないように変わったため，　`$ git clone https://github.com/Language-Media-Lab/100knock2021_huyu.git`は使えなくなりました．  
代わりに，ssh接続によるcloneが推奨されています．  
なので，まずはGithubでのssh接続の設定を行う必要があります．  

## GitHubでssh接続する手順
以下のサイトの手順通りにやるとできます．  
https://qiita.com/shizuma/items/2b2f873a0034839e47ce  
わからない点があればどんなことでもTAへ質問してください．  

# usage
以下はGithubでssh接続できている前提で書いています．
初回はこのレポジトリを clone してください。  　　
```
$ git clone git@github.com:Language-Media-Lab/100knock2021_huyu.git
```
  
各Chapterのはじめでは、各Chapterのディレクトリへ移動し、ブランチを切って、自分用の作業用ブランチで作業してください。  
ブランチの名前は自分の名前にしてください(例：北大太郎の場合、hokudai_taro)
```
# clone したディレクトリへ移動
$ cd 100knock2021_huyu
# 取り組むChapterへ移動
$ cd chapter01
#新規ブランチ作成
$ git branch hokudai_taro
#作成したブランチに切り替え
$ git checkout hokudai_taro
```

コードを書いたら自身のブランチの remote repository に push してください。  
- Pythonで書いた場合、ファイル名はすべて二桁の数字 & 自分の名前を入れてください（例: knock01_taro.py）
- google colabなどのJupyter Notebook等で書いた場合、ファイル名は各Chapterの数字 & 自分の名前を入れてください。（例: chapter01_taro.ipynb）
```
$ git add ./knockXX_taro.ipynb
$ git commit -m 'your message'
$ git push origin hokudai_taro
```
TAが毎週1章分コードのレビューを行い、問題がなければ、B3はmainブランチへマージしてください．  
**毎週各章のレビューとマージまで終わらせて，その日の勉強会を終わらせてください**

# 注意事項
わからないところはDiscord等で**積極的に** TA か研究室の人に聞いてください。     

# メモ・相談事項
- ファイル形式は.pyもしくは.ipynbが考えられるが、統一する? それとも混合でok?→混合でok
- 2021年度冬のチュートリアルでは各担当者のマージまではできませんでした（ファイル名が全員同名だったのでコンフリクトしてしまった）  
- →来年度はファイル名の末尾に自分の名前を入れるようにすると，コンフリクトが発生しないと思います
