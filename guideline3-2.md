# Understandable(理解可能)
https://www.w3.org/TR/WCAG21/#understandable

## Guideline 3.2 Predictable(予測可能)
https://www.w3.org/TR/WCAG21/#predictable

Webページを予測可能な方法で操作、閲覧できるようにする

### Success Criterion 3.2.1 On Focus
**A** user interface componentがfocusを受けた時、ウェブページの状態とかが変わってはいけない

この要件は認知障害や視覚障害を持った人が、意図しない状態の変化を起こす機会を減らす

例えばドロップダウンメニューをフォーカスした時に、そのドロップダウンメニューの選択肢が選択されてはいけない。

### Success Criterion 3.2.2 On Input
**A** 使用する前のユーザーへの説明なしに、user interface componentの設定が変更された時、自動的にその状態とかが変わってはいけない。

この基準の目的は、チェックボックスやテキストインプットなどのuser interface componentをユーザーが操作したときにその操作によっておこることが予測可能であることを保証すること。

チェックボックスとかのコンポーネントはそれに対してのアクションによって何らかの状態が変わる、この変更は視覚障害を持ってる方などの変更を認識しにくいユーザーに混乱を生じさせる可能性があるので、ちゃんとどういう変更が加わるかわかるようにしましょう

e.g. チェックボックスをチェックしたらウィンドウポップアップが発生するとか

### Success Criterion 3.2.3 Consistent Navigation
**AA** 複数のWebページで共通して繰り返されるナビゲーションメカニズムはユーザーが変更しない限り、相対的に同じ順番で表示されるようにしないといけない

これの意図は関連があるWebページ群の中で特定の情報を見つける必要がある人のために、一貫したレイアウト&デザインを提供することにある。
視覚障害者の方は画面の一部を拡大鏡を使って拡大しページの境界やわかりやすい目印などを使ってコンテンツを見つけたりしてるのでそういう点でも役に立つ

これによってユーザーが繰り返されるコンテンツ上で特定のコンテンツの場所を予測しやすくなったり再びそのコンテンツに出会ったときに迅速に見つけられるようになる。

### Success Criterion 3.2.4 Consistent Identification 
**AA** サービスなどのウェブページ群において同じ機能を提供しているコンポーネントは一貫性を持って特定できるようになっていなければならない

検索ボックスとかそのWebページで複数回使われていたり、サービスのWebページ群で複数回使われていたりするコンポーネントがある、そういった共通のコンポーネントを一貫性を持った方法(同じlaternative textを持つなど)で特定できるようにしなければいけない。

スクリーンリーダーを使っている方などは、そのコンポーネントの機能を把握するとき同じサービスの他のWebページで使われていたラベルからその機能を推測して使うことがある。そのため、ラベルなどのコンポーネントを特定するためのものは一貫性を持った方が良い

### Success Criterion 3.2.5 Change on Request 
**AAA** 状態の変化はユーザーのリクエストによってのみ行われるか、もしくはそういった変更をオフにする機能を持っている

ウィンドウが勝手に起動したり、リストから項目を選択したら勝手にフォームが送信されたりして、予期しない状態の変化が起こると運動機能障害を持っている方や、弱視・視覚障害の方などに混乱をもたらす可能性があるので状態の変更はユーザーからの明確なリクエストがあったときのみにしようねということ。

ただ、コンテンツの種類によっては意図したユーザー体験を提供するための自動で状態を変更することが必要な場合もあるからそれは許可してる(ユーザーの好みに応じて自動的に状態を変えるようなコンテンツとか)

**e.g. **
- 自動で更新されずに「update now」ボタンがある
- ユーザーに気づかれないレベルで古いページから新しいページにリダイレクトされる

