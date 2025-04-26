+++
date = '2025-04-26T10:21:28+09:00'
draft = false
title = 'My First Article'
+++

# 初めての記事

## Hugoの基本的な初期設定

Hugoで作ってみた。

高速でいいね。（MacProのせいかもだけど）

マークダウンでかけるのが普通に熱い

一応最初のコマンド載せておきます

<!--more-->

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

## Hugoの運用のための基本知識

1.
自分のプロジェクトとテーマのプロジェクトの二つがあり、それらの構造はほとんど同じである。
カスタマイズ性は確保されており、CSSや（多分）layoutsも変えれる。

2.
アンダーバーの意味については以下のイメージ図がわかりやすい。
URL: /post/
  → 表示されるのは
     - layouts/post/list.html でレイアウト
     - content/post/_index.md で本文を表示

URL: /post/first-article/
  → 表示されるのは
     - layouts/_default/single.html でレイアウト
     - content/post/first-article.md の本文

3.
```
<!--more-->
```
これでReadmoreの前の部分と後の部分を分けれる