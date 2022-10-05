# Operable(操作可能)
https://www.w3.org/TR/WCAG21/#operable

## Guideline 2.5 Input Modalities
https://www.w3.org/TR/WCAG21/#input-modalities

キーボード以外のさまざまな入力を通してユーザーが機能を簡単に操作できるようにする

### Success Criterion 2.5.1 Pointer Gestures
**A** 複数の指を使った操作やpath-based gesturesにより操作する機能は、一つの指での操作やpath-based gestureがなくても操作できるようにしましょう、複数の指を使った操作やpath-based gestureが必要不可欠な時は除きます

※path-based gestureとは、指で操作する際などにスタートのポイントからエンドのポイントまでスワイプ等でポインタを移動させる時に途中でそこを通らないといけないポイントがあるような操作の挙動(つまり3つ以上の点を通らないといけないスワイプ操作など)

ちなみにここで言ってる必要不可欠な場合とはウェブ上でやる署名とか

これを満たすことでデバイスの操作のために特別な機器(視線による操作ができるシステムや言葉によってマウスの操作ができるシステム)を使用している方が使いやすくなる

### Success Criterion 2.5.2 Pointer Cancellation
**A** single pointerで操作できる機能は以下の要件の内、最低一つは満たさないといけない
- No Down-Event: down-event(クリックのことと考えてよさそう)がいかなる機能の実行にも使われてない
- Abort or Undo: 機能が完了するときはup-event(クリックの上げた時)の時で、完了させる前に機能の実行を中断させる方法か、機能の実行が完了した後に戻せる機能を持っていること
- Up Reversal: up-eventは前に行ったdown-eventの結果を反転させる
- Essential: down-eventによる機能の実行の完了がessential(絶対必要)なとき

※single pointerはクリックやタップ、ダブルクリックなどスクリーン内の一つのポイントでつながっているポインタ

この要件はユーザーがポインタ操作をキャンセルできるようにするのを意図している。意図としては、いろんな障害を抱えてる方はうっかり望んでいないタッチやマウスのイベントを発生させてしまうことがある、その際に上の要件を満たせているとどうにかできる

jsのclickイベントはup-eventに実行される一例
up-eventの際に発火するようにするとそのクリック対象の要素からずらした後に離すと発火しない

### Success Criterion 2.5.3 Label in Name
**A** ラベルのついていて画像だろうがテキストだろうが文字を含んでいるuser interface componentsだったら、そのname(htmlタグのname属性とかコンピュータにそのコンポーネントを表すものとして伝わるテキスト)がラベルとして視覚的に表現されているものと同じでないといけない

### Success Criterion 2.5.4 Motion Actuation
**A** デバイスのmotion(動き)やユーザーのmotionによって操作される機能は、user interface componentsでも操作できるようにしないといけない、加えてmotionへの反応は不意の誤操作を防ぐためにオフにできなければいけない。ただし、これは以下の場合は除く
- Suppoted Interface: そのmotionがアクセシビリティについてサポートされたデバイスを通して操作できる場合
- essential: 機能としてmotionが絶対に必要な場合

例として挙げるとLINEのフルフルによる友達交換とかジャイロスコープによる操作とかがある

これによってデバイスをうまく動かせない人とかでも機能を操作できるようになるよね
