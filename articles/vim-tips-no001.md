---
title: "対になる動作のプレフィクスとして [] を利用する"
emoji: "💨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vimtips"]
published: true
---

Vimでは好みのキーバインドを自らで設定することができます。  
例えば、以下の例は`j` `k`キーを`gj` `gk`に置き換え表示行でのカーソル移動を実現します。  

```vim
nnoremap j gj
nnoremap k gk
```

バッファやタブ・QuickFixのエラー箇所の移動のような対になる動作のキーバインドは以下のように`[` `]`キーに割り当てると一貫した定義をすることが可能です。  

```vim
nnoremap [t :tabprevious<CR>
nnoremap ]t :tabnext<CR>
nnoremap [q :cprevious<CR>
nnoremap ]q :cnext<CR>
```

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](https://vim-jp.org/slacklog/C01JSLDQZH6/2021/01/#ts-1609907852.004700) @yutkat
> @yutkat  
> 意外と見落としがちだけど [ ] が対となる動作のプレフィックスとして使えます。  
> ```vim
> nnoremap [t           :tabprevious<CR>
> nnoremap ]t           :tabnext<CR>
> nnoremap [q           :cprevious<CR>
> nnoremap ]q           :cnext<CR> 
> ```

まとめ kato-k (@uvrub)

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
