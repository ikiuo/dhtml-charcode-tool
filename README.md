# 文字コードの変換と確認など

入力されたテキストを変換したり、文字コードの確認ができます。

- 正規化：NFC,NFD,NFKC,NFKD の各種で正規化します
  - 変換された文字は背景の色が変化します
- コードポイント：文字ごとに文字コードをルビとして表示します
- innerHTML：出力タグの innerHTML に代入します
  - 入力されたテキスト次第では正常動作しなくなるので注意してください
- 英数字の変換：ASCIIの英数文字をボールドやイタリックなどの文字コードに変換します（できない場合もあります）
  - "Sample" → "𝐒𝐚𝐦𝐩𝐥𝐞", "𝑆𝑎𝑚𝑝𝑙𝑒", "𝕊𝕒𝕞𝕡𝕝𝕖" など
- 円内文字への変換：円の中に該当文字があれば変換します
  - "SAMPLE 10" → "ⓈⒶⓂⓅⓁⒺ ⑩", "🅢🅐🅜🅟🅛🅔 ❿" など
- 丸括弧付き文字への変換：丸括弧で括られた文字との対応があれば変換します
  - "(祝) (A)(B)(C) (a)(b)(c) (10)" → "㈷ 🄐🄑🄒 ⒜⒝⒞ ⑽"
