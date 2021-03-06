---
title: "【Vim】動作の遅いVimを調査する"
emoji: "💨"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vimtips"]
published: true
---

Vimを利用しているとき、特定の動作が遲くなってしまうことがあるかもしれません。  
そのような時は以下のスクリプトを`.vimrc`に書き込んでおき、ログを取りたいタイミングで`:Profile`コマンドを利用すると良いでしょう。  

`Profile`コマンドが呼び出された後に実行された関数とスクリプトファイルを対象に、ログファイルが`~/profile.txt`に作成されます。  

```vim
command! Profile call s:command_profile()
function! s:command_profile() abort
  profile start ~/profile.txt
  profile func *
  profile file *
endfunction
```

`profile.txt`を開いた後、`:vim "Total time" %`・`:copen`を実行すると時間がかかった処理を探すのに役立つでしょう。

-------------------------------------------------------------------------------
元となった投稿: [Vim-jp Slack](https://vim-jp.org/slacklog/C01JSLDQZH6/2021/01/#ts-1610941456.003800) @hrsh7th
> @hrsh7th  
> command! Profile call s:command_profile()
> ```vim
> function! s:command_profile() abort
>   profile start ~/profile.txt
>   profile func *
>   profile file *
> endfunction
> ```
>
> なんか特定の処理が遅い気がする。。。って時に手軽に計測するコマンドを愛用しているので共有です。

まとめ kato-k (@uvrub)

この記事は[Github](https://github.com/kato-k/vim-tips)上で管理されています。情報の加筆・修正・記事の追加を歓迎します。
