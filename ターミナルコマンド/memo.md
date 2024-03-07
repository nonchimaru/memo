# ターミナルコマンド

-ターミナルからｖｓコードを開く方法

<pre>
code .
</pre>

# マージする

<pre>
git switch main
git pull origin main
git switch ブランチ名
git merge main
</pre>

# 誤ったブランチで開発を進めてしまった

現在のブランチがベースになってるため、現在のブランチが今回の変更点以外の作業分がコミットされてるなら良くない。

<pre>
git stash
git switch -c ブランチ名
git stash pop
git add .
git commit -m ""
git push origin ブランチ名
</pre>
