# Perceivable(知覚可能) 
https://www.w3.org/TR/WCAG21/#perceivable

## Guideline1.1 Text Alternative 代替テキスト
代替テキストを画像などのテキストでないコンテンツに渡すことでさまざまな障がい者のかたがそれぞれ記号や点字、音声、大きい文字など各々にあった形に変換できる

### Success Criteria(テキストでないコンテンツ)
以下の場合を除いてユーザーに見えている全ての非テキストコンテンツは代替テキストを持たないといけない

- Control, Input
  - これらは正しく作ればその意味を表すname（https://www.w3.org/TR/WCAG21/#dfn-name）を持つはずでそれにより十分アクセシブルになるから代替テキストが必要ない
    - ちなみにここでいうnameはname attributeではなくて、アクセシビリティの文脈でのname
    - ここでいうnameは基本的に見えなくてaccessible technologyにのみ情報が伝達されるもの
- Time-Based Media
  - 動画とか音楽とかのコンテンツに対してはそのコンテンツの説明だけを代替テキストとして設定する
  - Time-Based MediaはTime-Based Mediaでアクセシブルにする方法が定義されてるので
- Test
  - 根本的にその人の聴覚能力や視覚能力を問うようなもの
  - 例えば、英語のリスニングテストをやっているときは代替テキストでどんな英語を喋ってるか文字で見えたらテストの意味がなくなっちゃうよね
- Sensory(とても感覚的なもの): フルートの音色とか
  - コンテンツの概要の説明だけ代替テキストを用意すればいい
- CAPTCHA
  - CAPTCHAは人間であることを証明するためのものなのに、代替テキストを設定したらコンピュータが一瞬で判定できるようになっちゃう
- Decoration, Formatting, Invisible
  - 装飾とか見えないコンテンツとかはassistive technologyから見えないようにする形でいいよね
