# Conformance(適合性)
https://www.w3.org/TR/WCAG21/#conformance

WCAG2.1への適合について、どうなったら適合したと言えるかといったところや、a11yがサポートされているとはどういうことを言うのかを解説してる章

## Guideline5.3 Conformance Claims(Optional) 適合性の主張
それぞれの達成基準(Success Criteria)はひとつのWebページについて定義されている。しかし、conformance claim(適合していることの主張）はひとつのページ、連続したページ、関連した複数のページに対してして良い

### 5.3.1 Required Components of Conformance Claim
別に適合性を主張しなくても、WCAG2.1に適合したといえる。ただもしconformance claim(適合性を主張)したいのであれば、以下の情報を含まなければいけない
1. 主張した日
2. ガイドラインのタイトルとバージョンとURI
3. 適合のレベル(A, AA, AAA)
4. 主張するWebページ簡潔な説明(サブドメインが対象になるかも含めた適合を主張するWebページのURIの一覧等)
5. 適合するために依存しているウェブコンテンツ技術のリスト(HTMLとかCSSとかcanvasとかそういうイメージかな？)
