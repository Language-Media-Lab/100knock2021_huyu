# 言語処理100本ノック 2021年度 冬
言語メディア研2021年度新入生向け勉強会として、言語処理100本ノックに取り組みます。  
教材URL: https://nlp100.github.io/ja/  

参加学生(B3)
- 岡田さん
- 橋本さん
- 矢野さん

TA(チューター)
- TBA
- (坂田：自由参加だと参加学生の確保が呼びかけないと難しい&参加学生に偏りがあるので，毎週の担当制にしたいです)

## 勉強会の流れ

### B3がやること
【予習】  
- 次の週までに言語処理100本ノックの章を一つ（10問）終わらせて，GitHubにコードをアップする．  
- [問題文を記載しているJupiterNotebookテンプレート](https://github.com/Language-Media-Lab/100knock_template)を使用してください．
    - ※ファイル名は「[コードを書き終えたら]」(#コードを書き終えたら)の部分に従って変更してください．
    - (今後のTODO:来年は，初回レポジトリ作成時にこれらのテンプレートがはじめから入っているようにすると良いと思います)
- 答えを見ながらでもOK，TA(チューター)にコードの説明が出来るようにを意識する．  
- **分からない部分はTA(チューター)に訊く（重要）．** 
    - **訊くことは，チュートリアルの日以外でも大丈夫です！** (研究室の先輩へDM等) 
  
【当日】  
- 予め解いてきた問題のコードをTA(チューター)に説明する．  
- その際，分からない部分は気軽にTA(チューター)に訊ねてOK．  
- 毎回のB3チュートリアル終了後，**必ず**個人の各々の進捗をB3チュートリアルのテキストチャンネルに投稿してください．
    - 以下にテンプレートを示したので，こちらのコピペで大丈夫です．
>今週やった範囲と来週までに終わらせる範囲です．  
>今日までやった範囲：〇〇章まで完了  
>来週までに終わらせる範囲：〇〇章まで  

- (リモート時の場合)Discordで画面共有をお願いすると思うのですが，「配信画質」は「より読みやすいテキスト」の設定でよろしくお願いします．

<img src="https://user-images.githubusercontent.com/68231213/152498573-d337a0ed-19ac-4ee5-88ca-71c632f62468.png" width="300px">

【当日の参加ができない時】
- (なるべく早く) **必ず**B3チュートリアルのテキストチャンネルで参加ができない旨を伝えて，他の曜日にずらす等のリスケジュールをB3自ら行ってください．

【当日まで問題が解けなかった場合】
- スケジュール等の忙しさもあると思うので，連絡があれば遅れても大丈夫です
- 必ず連絡してください🙇‍♀️
- 連絡内容として「遅れてしまっているのですが，◯章の問◯番までできています」等の，問題の何番目までできているかをB3チュートリアルのテキストチャンネルに送ってください．
  
  
### TA(チューター)がやること
【予習】  
- B3から尋ねられた時に答えられるように復習しておく．  
  
【当日】  
- B3からコードの説明を聞く（B3ひとりにつきTA(チューター)ひとりがベスト）．  
- 分からない部分を訊かれたらがんばって教える．  
- 可読性の高いコードになるように修正する．
- 勉強会当日の最後に，来週までに〇〇章まで終わらせる等の目標を設定する．


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

## 初回
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

## コードを書き終えたら
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
