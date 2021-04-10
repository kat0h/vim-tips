---
title: "Vim scriptの関数を探す"
emoji: "💨" # 任意の絵文字を設定
type: "tech" # tech: 技術記事
topics: ["vimtips"] # Vim Topicと区別するため、"vimtips"のみ
published: true
---

Vim scriptには膨大な数の関数が実装されています。  
中にはVimならではの関数もあり、目当てのものを見付けるのは非常に骨の折れる作業です。  

そのような場合は以下のコマンドを利用するとよいでしょう。  
目当ての関数の上で`CTRL-]`をタイプすることで、関数の詳細な利用法を知ることができます。  

ヘルプ内での移動は、丁度ウェブブラウザの様にジャンプリストに記録され、`CTRL-O`・`CTRL-I`をタイプすることでジャンプリスト間を移動することができます。  

```vim
:h function-list
```

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](https://vim-jp.org/slacklog/CJMV3MSLR/2021/02/#ts-1613726265.328000) @obcat
> よかったです。ちなみに特定の機能を探すときは`:h function-list`が便利だったりします 🔎

まとめ kato-k

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
