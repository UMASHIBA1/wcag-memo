# Robust(堅牢性)
https://www.w3.org/TR/WCAG21/#robust

## Guideline 4.1 Compatible(互換性)
https://www.w3.org/TR/WCAG21/#compatible

現在・将来における支援技術を含んだユーザーエージェントに対する互換性を最大化する

### Success Criterion 4.1.1 Parsing
**A** マークアップ言語において実装されているコンテンツにおいて、仕様で許されている場合を除き以下の要件が満たされている
- 要素の開始タグと終了タグがちゃんとある
- 仕様に従って要素がネストされてる
- 要素が属性を重複して持っていない
- idが全てユニーク

正しい仕様に則ってないHTMLでもユーザーエージェントはrepair technologyを使って解釈してくれるけど、それは正しく機能するかわからないし、ユーザーエージェントの種類によっても動作が変わってしまうかもしれない、加えて支援技術が解釈できない可能性もある、だからちゃんとしたマークアップをしようねという話

### Success Criterion 4.1.2 Name, Role Value
**A** 全てのuser interface componentにおいて、
- そのnameとroleはprogrammatically determinedになっている
- ユーザーが設定することができるstatesとpropertiesとvaluesはprogrammatically setできる
- それらのアイテムの変更は支援技術を含んだユーザーエージェントが検知できる

これは支援技術がuser interface componentsの情報を集めたり、その状態の設定をしたり最新に保つのを目的としている

基本的にブラウザデフォルトのuser interface componentsを使ってたら問題ないけど、カスタムで珍しいコンポーネントを作るときはちゃんとブラウザや支援技術に状態を伝えられるような実装にしようねという話だと思ってる。

※programmtically set: 支援技術を含んだユーザーエージェントによってサポートされている方法を使ったソフトウェアで設定できること

### Success Criterion 4.1.3
**AA** マークアップ言語によって実装されたコンテンツにおいて、status messageをroleやプロパティを通じてprogrammatically determinedにし、focusなしでも支援技術を使ってユーザーに伝えられるようにしましょう！

※status message: changes of context(UAとかfocusとかviewportとか)の変更によって伝えられず、ユーザーが起こしたアクションが成功したかといったものやアプリケーションのpending状態、エラーの存在を伝えてくれる情報

この成功基準は、change of context(UAの更新とかfocusの移動とか)なく新しいコンテンツがページに追加された時のための基準になっている。
focusを奪うとうで十分支援技術に状態の変更が伝わるのでchange of contextが起こる変更はこの基準で考えなくていい

視覚障害などでスクリーンリーダーを使っている方が、このstatus messageがあることによって、コンテンツの状態に変化が起こった際に気づけるようになる、かつ、このstatus messageに対して属性(importantとかinfo)とかつけることによって認知障害などのある方が好きなタイミングで通知を鳴らせるようになったりするかもしれない

e.g. ECサイトでユーザーがショッピングカートに商品を入れた際に、右上のカートのアイコンのところに「5つのアイテムが入ってます」というポップアップが出るかもしれない、こういうのをstatus messageとしてユーザーに伝えたい

これの実装方法としてはrole=status等がある
