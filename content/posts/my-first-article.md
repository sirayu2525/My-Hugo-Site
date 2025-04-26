+++
date = '2025-04-26T10:21:28+09:00'
draft = false
title = 'My First Article'
+++

# 初めての記事

Hugoで作ってみた。

高速でいいね。（MacProのせいかもだけど）

マークダウンでかけるのが普通に熱い

一応最初のコマンド載せておきます

```
雛形の作成
hugo new site my-hugo-site

テーマの挿入
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke

リモートリポジトリと紐付け
git remote add origin https://github.com/sirayu2525/My-Hugo-Site.git

ローカルの現在のブランチを強制的にmainに変更
git branch -M main

最初のプッシュ
git add .
git commit -m "initial commit"
git push -u origin main

新しい記事の作り方
hugo new posts/NAME.md

```

きしょいエラーが出た時はリセットしよう

```
rm -r reosources
rm -r public
```

おすすめ記事
https://juggernautjp.info/getting-started/directory-structure/
