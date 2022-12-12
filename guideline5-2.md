# Conformance(適合性)
https://www.w3.org/TR/WCAG21/#conformance

WCAG2.1への適合について、どうなったら適合したと言えるかといったところや、a11yがサポートされているとはどういうことを言うのかを解説してる章

## Guideline5.2 Conformance Requirements
WCAG2.1に適合しているというためには以下の全ての要件を満たさないといけない

### 5.2.1 Conformance Level
以下のいずれかの適合レベルが完全に満たされている必要がある
- Level Aの要件を満たしているというためには: 全てのLevel AのSuccess Criterionを満たしている必要がある、もしくは全てのLevel AのSuccess Criterionを満たしているalternate versionがある必要がある
- Level AAの要件を満たしているというためには: Level Aで言ってるきほんてきに同じ、変わったところはAとAAの二つになったところ
- Level AAAの要件を満たしているというためには: Level AAで言ってるきほんてきに同じ、変わったところはAとAA, AAAの三つになったところ

※alternative version: そのLevelに適合していて同一情報・同一機能を同じ言語で提供していて、完全に同じ情報を提供しており、以下のうちひとつを満たすもの
- alternative versionにa11y技術を使って到達できる
- 非適合のバージョンは適合しているalternative versionからしか到達できない
- 非適合のバージョンは適合しているalternative versionに到達するための機能を提供している適合ページからしか到達できない

### 5.2.2 Full Pages
適合(Conformance)しているというためには全てのページがそのa11yレベルに適合されていないといけない、一部のWebページが除外されていたらそれは適合されているとは言えない

注意点3点
- 代替となるコンテンツがあってそれが代替元のWebページから辿れる場合は別
- もしページ内のコンテンツが筆者のコントロールが効かないものだったら5.4のStatement of Partial Conformanceを参照しよう
- レスポンシブのWebページとかのいろんな画面サイズで表示されるWebページの場合その全てのバリエーションで適合してなければ適合しているとは言えない


### 5.2.3 Complete processes
Webページがあるプロセス(ECサイトの商品購入プロセスとか)の一部であった場合、そのプロセス内の全てのWebページが特定のレベルに適合してなければ、適合していると言えない
