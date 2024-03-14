- `button` or `a`
  - https://marcysutton.com/links-vs-buttons-in-modern-web-applications
    - `a`
      - https://developer.mozilla.org/ja/docs/Web/HTML/Element/a
      - 無効にはできない
        - `tabindex`と`aria-hidden`で不活性にはできる
        - roleは`link`
    - `button`
      - https://developer.mozilla.org/ja/docs/Web/HTML/Element/button
      - roleは`button`
    - スクリーンリーダーのユーザーが、「ボタンを押して」と案内されてもそれが`a`でマークアップされていたら混乱する可能性がある
  - https://www.webaxe.org/proper-use-buttons-links/
    - > The main point is, please do the basics.
  - https://itstiredinhere.blogspot.com/2014/08/the-anchor-button-bad-for-accessibility.html
  - https://heydonworks.com/article/reinventing-the-hyperlink/
  - https://css-tricks.com/a-complete-guide-to-links-and-buttons/
    - クイックガイドライン
      - 別ページへ遷移するなら`a`
      - JSによる動作なら`button`
      - formの送信なら`input type='submit'`
    - `button`
      - formの中ならsubmitがデフォルトの挙動
        - formの外ならデフォルトの挙動は特に無い
      - 意味のある`href`がないときに使うと良い
        - 遷移先がない時
    - `a`
      - `href`がないとき、無効にするようなCSSを書くこともできる
        - ```css
          a:not([href]) {
            /* style a "disabled" link */
          }
          ```
      - `target="_blank"`で新しいウィンドウを開くのはあまり薦められない
        - 現在のページの作業を失わせないような状況くらいが適切なユースケース
          - もしくは技術的な何かの理由
        - https://adrianroselli.com/2020/02/link-targets-and-3-2-5.html
