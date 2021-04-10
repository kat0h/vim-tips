---
title: "【Vim】Unicodeをコードポイントから入力する"
emoji: "💨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vimtips"]
published: true
---

Vimの入力モードでは`<C-v>`を利用することで`<ESC>`等の制御文字を直接入力することができます。  
これは、Makefileなどを記述する際に設定に関係なくTab文字を入力するなどの使い方ができます。  
同じく`<C-v>`では直接文字コードの入力が可能です。`:h i_CTRL_V_digit`  
例えば`<C-v>u3042`と入力すると、ひらがなの「あ」が入力されます。  

この方法はわかりやすいですが、入力中の文字が見えない欠点があります。  
これを改善するために以下のマップを利用できます。  

```vim
inoremap <C-v>u <C-r>=nr2char(0x)<Left>
```

`<C-r>=`は直後に続くVim scriptの式を評価し、結果を挿入します。`ne2char()`はコードポイントを引数に取り、文字を返しますので同等の入力をわかりやすく利用できます。

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](https://vim-jp.org/slacklog/C03C4RC9F/2021/03/#ts-1616554467.468200) @monaqa
> @monaqa  
> mattn さんのコメントを聞いて
> ```vim
> inoremap <C-v>u <C-r>=nr2char(0x)<Left>
> ```
> とやってみたら便利になるかも、とふと思った

まとめ kato-k (@uvrub)

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
