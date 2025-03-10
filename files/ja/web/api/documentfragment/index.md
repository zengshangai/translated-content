---
title: DocumentFragment
slug: Web/API/DocumentFragment
---

{{ APIRef("DOM") }}

**`DocumentFragment`** インターフェイスは、親ノードを持たない最小限の文書オブジェクト (文書の断片) を表します。これは {{domxref("Document")}} の軽量版として使用され、標準の文書のようにノードで構成される文書構造の区間を格納します。重要な違いは、文書の断片はアクティブな文書ツリー構造の一部ではないため、断片に対して変更を行っても、文書に影響したり、{{Glossary("reflow", "再フロー")}}を起こしたり、変更が行われたときに性能上の影響を及ぼしたりすることがないことです。

`DocumentFragment` の一般的な利用方法は、まず一つ作成し、その中に DOM のサブツリーを構成し、 {{domxref("Node")}} インターフェイスの {{domxref("Node.appendChild", "appendChild()")}} または {{domxref("Node.insertBefore", "insertBefore()")}} などのメソッドを利用して断片を DOM に追加または挿入することです。こうすると断片のノードは DOM に移動し、空の `DocumentFragment` が残ります。すべてのノードが文書に一括で挿入されるため、それぞれのノードが別個に挿入されれば、その度に再フローや描画が起動する可能性があるところが、この場合は一度しか起動されません。

このインターフェイスはウェブコンポーネントでも大いに役に立っています。 {{HTMLElement("template")}} 要素はその {{domxref("HTMLTemplateElement.content")}} プロパティに `DocumentFragment` を含みます。

空の `DocumentFragment` は {{domxref("document.createDocumentFragment")}} メソッドやコンストラクターを使って作成できます。

{{InheritanceDiagram}}

## プロパティ

_このインターフェイスには固有のプロパティはありませんが、その親である {{domxref("Node")}} のプロパティを継承し、 {{domxref("ParentNode")}} インターフェイスのプロパティを実装しています。_

- {{ domxref("ParentNode.children") }} {{readonlyInline}}{{experimental_inline}}
  - : `DocumentFragment` オブジェクトの子である型 {{domxref("Element")}} のすべてのオブジェクトを含む、「生」の {{domxref("HTMLCollection")}} を返します。
- {{ domxref("ParentNode.firstElementChild") }} {{readonlyInline}}{{experimental_inline}}
  - : `DocumentFragment` オブジェクトの最初の子である {{domxref("Element")}}、または無ければ `null` を返します。
- {{ domxref("ParentNode.lastElementChild") }} {{readonlyInline}}{{experimental_inline}}
  - : `DocumentFragment` オブジェクトの最後の子である {{domxref("Element")}}、または無ければ `null` を返します。
- {{ domxref("ParentNode.childElementCount") }} {{readonlyInline}}{{experimental_inline}}
  - : `DocumentFragment` が持つ子の数を表す `unsigned long` を返します。

## コンストラクター

- {{ domxref("DocumentFragment.DocumentFragment()", "DocumentFragment()") }} {{experimental_inline}}
  - : 空の `DocumentFragment` オブジェクトを返します。

## メソッド

_このインターフェイスはその親である {{domxref("Node")}} のメソッドを継承し、 {{domxref("ParentNode")}} インターフェイスのメソッドを実装しています。_

- {{domxref("DocumentFragment.querySelector()")}}
  - : `DocumentFragment` の中で、文書の順序で見た場合に、指定されたセレクターに一致する最初の {{domxref("Element")}} ノードを返します。
- {{domxref("DocumentFragment.querySelectorAll()")}}
  - : `DocumentFragment` の中で、指定されたセレクターに一致するすべての {{domxref("Element")}} ノードの {{domxref("NodeList")}} を返します。
- {{domxref("DocumentFragment.getElementById()")}}
  - : `DocumentFragment` の中で、文書の順序で見た場合に、指定された ID に一致する最初の {{domxref("Element")}} ノードを返します。

## 仕様書

| 仕様書                                                                                                   | 状態                                         | 備考                                                               |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------ |
| {{SpecName('DOM WHATWG', '#interface-documentfragment', 'DocumentFragment')}} | {{Spec2('DOM WHATWG')}}             | コンストラクターと {{domxref("ParentNode")}} の実装を追加。 |
| {{SpecName('Selectors API Level 1', '#the-apis', 'DocumentFragment')}}             | {{Spec2('Selectors API Level 1')}} | `querySelector()` と `querySelectorAll()` メソッドを追加。         |
| {{SpecName('DOM3 Core', 'core.html#ID-B63ED1A3', 'DocumentFragment')}}             | {{Spec2('DOM3 Core')}}                 | {{SpecName('DOM2 Core')}} より変更なし                      |
| {{SpecName('DOM2 Core', 'core.html#ID-B63ED1A3', 'DocumentFragment')}}             | {{Spec2('DOM2 Core')}}                 | {{SpecName('DOM1')}} より変更なし                          |
| {{SpecName('DOM1', 'level-one-core.html#ID-B63ED1A3', 'DocumentFragment')}}     | {{Spec2('DOM1')}}                     | 初回定義                                                           |

## ブラウザーの対応

{{Compat("api.DocumentFragment")}}

## 関連情報

- [DOM インターフェイスの目次](/ja/docs/Web/API/Document_Object_Model)
