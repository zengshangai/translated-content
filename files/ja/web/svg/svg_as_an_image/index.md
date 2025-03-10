---
title: 画像としての SVG
slug: Web/SVG/SVG_as_an_Image
---

SVG 画像は、様々な場面で画像形式の一つとして使用することができます。多くのブラウザーは SVG 画像を以下の場所で対応しています。

- HTML の {{HTMLElement("img")}} または {{SVGElement("svg")}} 要素
- CSS の {{cssxref("background-image")}}

## Gecko 固有の場所

さらに、 Gecko 2.0 {{geckoRelease("2.0")}}では次の場所でも SVG の使用に対応しています。

- CSS の {{cssxref("list-style-image")}}
- CSS の {{cssxref("content")}}
- SVG の {{SVGElement("image")}} 要素
- SVG の {{SVGElement("feImage")}} 要素
- Canvas の [`drawImage`](/ja/docs/HTML/Canvas/Tutorial/Using_images#drawImage) 関数

### 制限

セキュリティ上の目的で、 Gecko は SVG コンテンツを画像として扱う場合にいくつかの制限を設けています。

- [JavaScript](/ja/docs/JavaScript) は無効になります。
- 外部のリソース (画像やスタイルシートなど) を読み込むことはできませんが、 data: URI を使用してインライン化されていれば可能です。
- {{cssxref(":visited")}}-のリンクスタイルは描画されません。
- プラットフォームネイティブのウィジェットのスタイル付け (OS のテーマに基づくもの) は無効です。

なお、上記の制限は画像のコンテキストに限定されたものです。 SVG コンテンツが直接表示された場合、または {{HTMLElement("iframe")}}, {{HTMLElement("object")}}, {{HTMLElement("embed")}} の何れかの要素を使用して文書として埋め込まれた場合には適用されません。

## 仕様書

| 仕様書                                                                                                                                   | 状態                                     | 備考                                                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------- |
| {{SpecName("HTML5 W3C", "embedded-content-0.html#the-img-element", "SVG within &lt;img&gt; element")}} | {{Spec2("HTML5 W3C")}}             | {{HTMLElement("img")}} 要素内の SVG の使い方を定義。                   |
| {{SpecName("CSS3 Backgrounds", "#the-background-image", "SVG within 'background-image' CSS property")}} | {{Spec2("CSS3 Backgrounds")}} | {{cssxref("background-image")}} プロパティ内の SVG の使い方を定義。 |

## 関連情報

- [HTML 内の SVG 入門](/ja/docs/SVG_In_HTML_Introduction)
