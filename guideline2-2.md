# Operable(操作可能)
https://www.w3.org/TR/WCAG21/#operable

## Guideline 2.2 Enough Time
https://www.w3.org/TR/WCAG21/#enough-time

ユーザーに対してコンテンツを、使い・読むのに十分な時間を与える

### Success Criterion 2.2.1 Timing Adjustable
**A** コンテンツを読める時間に制限を設けているなら以下のうちの一つに当てはまらないといけない
- Turn off: ユーザーがそのコンテンツを見る前にその時間制限をオフにする機能を提供する
- Adjust: ユーザーがそのコンテンツを見る前に最低そのコンテンツのデフォルトの10倍の時間は見れる時間を調整できないといけない
- Extend: ユーザーがスペースバーを押すみたいな簡単なアクションで時間制限を延長できるようにしないといけなくて、さらにその時間制限の20秒前には時間制限が来ることの警告をしないといけない、かつその延長は合計で最低10分までは延長できるようにしないといけない
- Real-time Exception: 時間制限がオークションみたいなリアルタイムなイベントに設けられたものだったらその場合はいい感じに対応できなくてもしょうがない
- Essential Exception: その時間制限がコンテンツを提供する上で必要不可欠なもので、時間延長したらドメイン的に正しくないものになってしまう場合(チケット購入サイトとか)
- 20 hour Exception: タイムリミットまで20時間以上あるようなら気にしなくていいよ

ただ、タイムリミットをつけているコンテンツよりタイムリミットがないコンテンツの方がより良いものではある

この項目の対象は様々な障害などでタイムリミットが来る前に反応することが難しい人

### Success Criterion 2.2.2: Pause, Stop, Hide
**A** 情報が移動やスクロール、点滅や自動的な更新などをしてしまう場合は以下を満たさないといけない
- 移動, 点滅、スクロールの場合: 以下の三つの項目に当てはまってしまう場合、かつコンテンツの情報や機能に不可欠なものでない限り、一時停止や停止、もしくは隠せるようにしないといけない
  1. 自動的に再生される
  2. 5秒以上続く
  3. 他のコンテンツと並行して表示されている
- 自動的な更新の場合: 以下の二つに当てはまってしまう場合はユーザーに一時停止や停止、コンテンツを隠す機能や自動更新の頻度を調節する機能を提供しなければいけない
  1. 自動的に再生される
  2. 他のコンテンツと変更して表示されている

認知障害等でアニメーションがあるとコンテンツに集中できない方のための項目

### Success Criterion 2.2.3 No Timing
**AAA** リアルタイムイベントというどうしようもないものを除いて時間制限付きのインタラクションを求めるようなコンテンツを提供しない
基本的に2.1.1の強化版っぽい

ちなみに動画とか手話とかはGuideline1.1でカバーされていて、同じ内容のテキストとか代替となる手段があれば良いという感じらしい

### Suceess Criterion 2.2.4 Interruptions
**AAA** 緊急事態の際を除いて中断されることをユーザーが延期もしくは保留することができる

中断というのはWebsocketとかを使ったサーバーからの自動更新とかを中断できるということだと思う。

Twitterとかのタイムラインが読んでるのに自動で更新されて流れちゃうみたいなのを想像すれば良さそう

注意力等に影響する障害を持っている方などは文章などを読んでいた時に自動で中断されたらその後また読み直すのがすごい大変だよね

### Success Criterion 2.2.5 Re-authenticating
**AAA** セッションの認証が切れた際に、ユーザーがもう一度再認証すれば再度行っていた操作をそのまま継続することができる

まぁ、普通にこれできると便利だし、認知的な障害を持っている方やボイスオーバーを使って操作している方はより操作に時間がかかるからセッションが切れてしまう確率が上がる。そのためにもやりましょう

### Success Criterion 2.2.6 Timeouts
**AAA** データが保存されなくなる(損失する)時間についてユーザーに対して警告される、ただし、２0時間以上ユーザーが操作してなくてもデータが損失しない場合は警告を出さなくてもよい

認知障害を持っている方はオンライン上でするべきプロセスを完了させるためにも多くの時間がかかる場合がある。
そういった方が休憩などを取りながらも操作できるようにしたい
この基準の一番良い達成方法は２0時間以上データを保持し続けられること

ただし、この項目はコンテンツプロバイダが干渉し得る範囲のみで行えばよくて、ユーザーがブラウザのタブを閉じてしまったとかは考慮しなくても良い