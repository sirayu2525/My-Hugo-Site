+++
date = '2025-04-26T18:29:53+09:00'
draft = false
title = 'My First Site'
+++
# 初めてサイトを作ったので共有する

## 経緯

大学にまめちしきなどの情報を取りまとめて、発信している個人のツイッターがある。
その人に頼まれて、豆知識をまとめる形でサイト制作を依頼された。

## 採用技術および使用ツール

１００％Next.jsで作成
VPSにホスティング（今思えばVercelでも良かったかも）
Supabaseをデータベースとして採用。
　（Team機能などで部活全体で管理がしやすい。）
<!--more-->
https://hamubasu.com
![hamubasu](/images/ハムバス.png)


## 全体の構造

コンポーネント開発を基本とする。再利用できるものが多かった。
https://hamubasu.com

![hamubasu](/images/hamubasu.png)

## Next.jsについて

AppRouterを採用しました。
PagesRouterの問題の一つであるバケツリレー（Props Drilling）が起きやすそうな構造。
(実際は、page.tsxでデータフェッチしてそれをpropsでArticleListのコンポーネントに渡していてバケツリレーしてしまった)

サーバー側での処理（データフェッチ等）がメインだったので、ＲＳＣの思想とも合致する。






## 改善点

> App RouterではServer Componentsでのデータフェッチが利用可能なので、
> できるだけ末端のコンポーネントへデータフェッチをコロケーションすることを推奨しています
とあるのでpage.tsxでするのはあまりよろしくない。

RouteHandlerをサーバーサイドで使ってしまっている。

## 感想



