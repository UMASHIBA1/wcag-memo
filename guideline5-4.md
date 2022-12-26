# Conformance(適合性)
https://www.w3.org/TR/WCAG21/#conformance

WCAG2.1への適合について、どうなったら適合したと言えるかといったところや、a11yがサポートされているとはどういうことを言うのかを解説してる章

## Guideline5.4 Statement of Partial Conformance - Third Party Content
メールやSNS、ニュースサイトなど、時間の経過とともに自動的に他のソースからコンテンツが追加されるWebページがあります。
こういうページの場合、他のソースから生成されるコンテンツ(uncontrolled cotent)がどういうものになるか最初の段階ではわかりません。ただこういったuncontrolled contentは自前のコンテンツ(controlled content)のアクセシビリティにも影響を与えることがあります。

そしてこういった場合にガイドラインに適合させるためには以下の二つの選択肢があります。

1. しっかりとして知識に基づいて、適合性の判断をする
  - uncontrolled contentを監視して2営業日以内にガイドラインに適合していないものを修正、もしくは削除した場合、その修正もしくは削除対応中のものを除いてそのページはガイドラインに適合しているので、「適合していると」主張できる
  - 不適合なコンテンツを監視したり修正したりするのが不可能な場合はもちろん適合性は主張できないよ
2. 部分適合の主張をする
  - Webページ全ては適合してないが、特定の部分(この場合uncontrolled content?)を削除すれば適合することができるという主張はできる。
  - 主張の仕方としては「このページは適合していないけど管理外のソースから生成された以下の部分が削除されればlevel AでWCAG2.1に適合する」みたいな感じになる
  - さらに部分的な適合を主張したければuncontrolled contentについて以下の二つについてもその主張の中でしっかりと説明されていなければいけない
    - このコンテンツはサイトのオーナーの管理外にあること
    - ユーザーがどの部分が適合していないのかちゃんとわかるようになってること(「自分達が管理してない全ての部分」みたいなざっくりした書き方じゃダメだよってこと)