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

