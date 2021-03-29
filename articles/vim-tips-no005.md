---
title: "nNコマンドの挙動を自然にする"
emoji: "💨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vimtips"]
published: true
---

Vimの検索には、マッチを前方から行う`/`と後方から行う`?`があります。  
マッチした対象の移動には`n``N`を利用しますが、`/`と`?`で移動の方向が変わり直感的でないことがあります。  
この挙動を変更したい場合以下のスクリプトを`.vimrc`に書くと良いでしょう。  

```vim
nnoremap <expr> n 'Nn'[v:searchforward]
nnoremap <expr> N 'nN'[v:searchforward]
```

上のスクリプトは検索の方向によっての値の変わる`v:searchforward`を利用して`n``N`のどちらのキーを展開するか決定します。  

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](https://vim-jp.org/slacklog/C03C4RC9F/2021/01/#ts-1611373043.021300) @yutkat
> @yutkat  
> ```vim
> nnoremap <expr> n  'Nn'[v:searchforward]
> nnoremap <expr> N  'nN'[v:searchforward]
> ```

まとめ kato-k (@uvrub)

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
