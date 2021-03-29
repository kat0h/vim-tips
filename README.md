# Vim-tips

Vim-jp Slackで話題に上ったVimの便利な使い方をまとめた記事です。  
記事はZennで見ることができます。
[Zenn (Topic: vimtips)](https://zenn.dev/topics/vimtips)

## Articles

| filename | title |
| -- | -- |
| [articles/vim-tips-no001.md](articles/vim-tips-no001.md) | 対になる動作のプレフィクスとして"[]"を利用する |
| [articles/vim-tips-no002.md](articles/vim-tips-no002.md) | Unicodeをコードポイントから入力する |
| [articles/vim-tips-no003.md](articles/vim-tips-no003.md) | カラースキームによって一部の行が塗りつぶされてしまったとき |
| [articles/vim-tips-no004.md](articles/vim-tips-no004.md) | 動作の遅いVimを調査する |
| [articles/vim-tips-no005.md](articles/vim-tips-no005.md) | nNコマンドの挙動を自然にする |

## 記事の書き方

### 対象となるTips
Vim-jp Slack上に投稿されたVimに関する設定・利用法など。  
または、Vimに関する便利な知識。  

### ファイル名
`articles/`下に連番で配置してください。

### フォーマット
``` md
---
title: "タイトル"
emoji: "💨" # 任意の絵文字を設定
type: "tech" # tech: 技術記事
topics: ["vimtips"] # Vim Topicと区別するため、"vimtips"のみ
published: true
---

本文

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](SlackLogへのリンクを記入) @発言者のid
> 元のpostを原文のママ貼り付け

まとめ まとめた本人のidを記入

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
```
記事が正しく書けているかは`zen-cli`を用いて確認してください。

### 注意する点
Vim-jp Slack上の発言はCC-4.0ライセンスとされているが、記事を作成する前に以下の点を確認すること。  
- 発言者の了承を取る

PR is welcome
