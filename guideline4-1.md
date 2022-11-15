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

基本的にブラウザデフォルトのuser interface componentsを使ってたら問題ないけど、カスタムで珍しいコンポーネントを作るときは気をつけようねという話だと思う

※programmtically set: 支援技術を含んだユーザーエージェントによってサポートされている方法を使ったソフトウェアで設定できること

