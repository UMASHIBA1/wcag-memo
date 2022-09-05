# Operable(操作可能)
https://www.w3.org/TR/WCAG21/#operable

## Guideline 2.1 Keyboard Accessible
https://www.w3.org/TR/WCAG21/#keyboard-accessible

### Success Criterion 2.1.1 Keyboard
**A** 全ての機能的なコンテンツがキーボードを通してアクセスできる

目が見えない人のための機能
ダブルクリックみたいに短い時間に複数回キーを押さなければいけないといったようなものになってはいけない
ただし手書き機能のような基礎となっていてキーボードで操作するのが無理なものは除く

### Success Criterion 2.1.2 No Keyboard Trap
**A** ページ内のコンテンツに含まれるcomponentに対するfocusをキーボードで移動させられる場合、そのfocusは同じくキーボードのみで離れられるようにしないといけない
もしタブ操作や矢印キーなどの標準的なキーボード操作以外の操作方法をユーザーに求める場合はフォーカスを移動させるやり方をしっかりとユーザーに通知する必要がある

### Success Criterion 2.1.3 Keyboard(No Exception)
**AAA** 基本的に2.1.1と同じ、ただしこの成功指標を達成するためには**全て**のコンテンツがキーボードにより操作可能である必要がある、例外はない

2.1.1は手書き機能みたいな操作方法がキーボードによって操作できないことを許可してたけど、ここの成功基準では許可しない、そういう機能を入力手段として使ったらこの成功基準はもうクリアできない
(ちなみに手書き機能みたいなのをキーボードで操作できるようにしろよみたいな意図ではない)

### Success Criterion 2.1.4 Character KeyShortcuts
**A** 文字や句読点、数字、記号のみを使ってキーボードショートカットをコンテンツに実装した際は、以下のいずれか一つに当てはまらないといけない
- turn off: ショートカットを無効化できる
- Remap: ショートカットを一つかそれ以上のnon-printable keyboard character(Ctrl, Alt)に再マッピングできなければいけない
- Active only on focus: user interface componentを操作している場合そのコンテンツに対してfocusが当たっている時だけショートカットがアクティブになる

