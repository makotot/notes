# JSX

- jsxとは`React.createElement(component, props, ...children)`のシンタックスシュガー
- https://babeljs.io/repl/ でjsxがどのように変換されるかは確認できる
- JavaScriptにhtmlのようなコードを記述できる
- 構文はhtmlに近い
- jsxからjsへとトランスパイルしておき、ブラウザーではjsとして扱うようにする
  - トランスパイルはbabelやtypescriptで
- トランスパイルが`React.createElement`になるとは限らない
  - https://ja.legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html
  - react v17からは新しいトランスフォームがサポートされた
    - `react/jsx-runtime`
      - jsxのためだけにreactをimportする必要はない
    - https://github.com/reactjs/rfcs/blob/createlement-rfc/text/0000-create-element-changes.md#detailed-design
- jsxはreactだけで使うものではない
  - https://ja.vuejs.org/guide/extras/render-function#jsx-tsx

--- 

- https://ja.legacy.reactjs.org/docs/jsx-in-depth.html
- https://jasonformat.com/wtf-is-jsx/
- https://zenn.dev/sa2knight/scraps/105fa360d243b0
- https://kinsta.com/jp/knowledgebase/what-is-jsx/