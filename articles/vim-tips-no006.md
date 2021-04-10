---
title: "【Vim】細かい単位でUndoをする"
emoji: "💨" # 任意の絵文字を設定
type: "tech" # tech: 技術記事
topics: ["vimtips"] # Vim Topicと区別するため、"vimtips"のみ
published: true
---

Vimではモードの切り替えを単位としてUndoが働きます。  
ですので、Insertモードで<C-w>等の操作を行った場合はUndoの単位にならないので不便に思うことがあるかもしれません。  
その際は以下のスクリプトを利用すると良いでしょう。  

```vim
" Undoポイントの設置
inoremap <silent><C-w> <C-g>u<C-w>
inoremap <silent><C-u> <C-g>u<C-u>
inoremap <silent><C-m> <C-g>u<C-m>
```

`<C-g>u`は任意の場所でUndoの単位を付けるコマンドです。  

-------------------------------------------------------------------------------
まとめ kato-k (@uvrub)

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
