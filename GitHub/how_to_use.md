# Git の基本コマンドのまとめ

## ローカルの基本操作

1. 初期化
<br>ローカルリポジトリの新規作成
　<pre>
$ git init
</pre>
2. 変更履歴を記録
   <pre>
   $ git add .
   </pre>
   <pre>
   $ git commit -m "コミットメッセージ"
   </pre>
3. 状況確認
   <br> リポジトリとワークツリーの差分をチェック
   <pre>
   $ git diff
   </pre>
   リポジトリとステージの差分をチェック
   <pre>
   $ git diff -staget
   </pre>
   変更ファイルの確認
   <pre>
   $ git status
   </pre>
4. 履歴の確認
　<pre>
$ git log
</pre>
5. もとに戻す
   <br>ワークツリーの変更を取り消す
   <pre>
   $ git restore <ファイル名>
   </pre>
   ステージに上げた変更をワークツリーに戻す
   <pre>
   $ git restore -staget <ファイル名>
   </pre>

## GitHub でチーム開発する方法

### ブランチの仕組み

1. ブランチの作成
　 <pre>
$ git branch <ブランチ名>
</pre>
2. 一覧を表示
   <pre>
   $ git branch
   </pre>
   <pre>
   $ git branch -a
   </pre>
3. ブランチを切り替える
   <pre>
   $ git switch <ブランチ名>
   </pre>
   ブランチを新規作成して切り替え
   <pre>$ git switch -c <ブランチ名>
   </pre>
4. 変更をマージ
   <pre>
   $ git merge <ブランチ名>
   </pre>
   <pre>
   $ git merge main<ブランチ名>
   </pre>
5. コンフリクトの解消

- ファイルの内容を修正
- <<,==,>>を削除 ##

## GitHub との通信

1. 初期設定
   <pre>
   $ git config -giobal user.name(名前)
   </pre>
   <pre>
   $ git config -global user.email(メアド)
   </pre>
2. リモートリポジトリの追加
　<pre>
$ git remote add origin URL(リモート URL)
</pre>

### プッシュ・プル・フェッチ

- プッシュ →GitHub 上にコードをアップすること
- 他のローカルで行われたプッシュを自分のローカルに取り込むこと
- ローカルのリポジトリに対して GitHub の内容を取ってくること
  <br>リモートリポジトリにプッシュ
  <pre>
  $ git push origin <ブランチ名>
  </pre>
  リポジトリから情報収取
  <pre>
  $ git pull origin <ブランチ名>
  </pre>
  リモートリポジトリから情報収取
  <pre>
  $ git fetch origin
  </pre>
