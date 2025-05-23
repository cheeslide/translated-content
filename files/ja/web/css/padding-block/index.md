---
title: padding-block
slug: Web/CSS/padding-block
l10n:
  sourceCommit: fab1f9cef824066b3ce6a5b25f6c6db539f5d042
---

{{CSSRef}}

**`padding-block`** は [CSS](/ja/docs/Web/CSS) の[一括指定プロパティ](/ja/docs/Web/CSS/CSS_cascade/Shorthand_properties)で、論理的なブロック方向の先頭と末尾のパディングを設定します。これは要素の書字方向やテキストの向きに応じて物理的なパディングに変換されます。

{{InteractiveExample("CSS Demo: padding-block")}}

```css interactive-example-choice
padding-block: 10px 20px;
writing-mode: horizontal-tb;
```

```css interactive-example-choice
padding-block: 20px 40px;
writing-mode: vertical-rl;
```

```css interactive-example-choice
padding-block: 5% 10%;
writing-mode: horizontal-tb;
```

```css interactive-example-choice
padding-block: 2em 4em;
writing-mode: vertical-lr;
```

```html interactive-example
<section id="default-example">
  <div class="transition-all" id="example-element">
    <div class="box">
      Far out in the uncharted backwaters of the unfashionable end of the
      western spiral arm of the Galaxy lies a small unregarded yellow sun.
    </div>
  </div>
</section>
```

```css interactive-example
#example-element {
  border: 10px solid #ffc129;
  overflow: hidden;
  text-align: left;
}

.box {
  border: dashed 1px;
  unicode-bidi: bidi-override;
}
```

## 構成要素のプロパティ

このプロパティは以下の CSS プロパティの一括指定です。

- {{cssxref("padding-block-start")}}
- {{cssxref("padding-block-end")}}

## 構文

```css
/* <length> 値 */
padding-block: 10px 20px; /* 絶対的な長さ */
padding-block: 1em 2em; /* テキストの大きさに対する相対値 */
padding-block: 10px; /* 先頭と末尾の両方を設定 */

/* <percentage> 値 */
padding-block: 5% 2%; /* 直近のブロックコンテナーの幅に対する相対値 */

/* グローバル値 */
padding-block: inherit;
padding-block: initial;
padding-block: revert;
padding-block: revert-layer;
padding-block: unset;
```

`padding-block` プロパティでは、1 つまたは 2 つの値を指定できます。1 つの値が指定された場合は、 {{cssxref("padding-block-start")}} と {{cssxref("padding-block-end")}} の両方の値として使用されます。2 つの値が指定された場合、1 つ目の値が {{cssxref("padding-block-start")}} に、2 つ目の値が {{cssxref("padding-block-end")}} に使用されます。

### 値

`padding-block` プロパティは、 {{CSSxRef("padding-left")}} プロパティと同じ値を取ります。

## 解説

これらの値は、 {{cssxref("padding-top")}} と {{cssxref("padding-bottom")}}、または {{cssxref("padding-right")}} と {{cssxref("padding-left")}} プロパティに、 {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}} で定義された値に従って対応します。

## 公式定義

{{cssinfo}}

## 形式文法

{{csssyntax}}

## 例

### 縦書きテキストにおけるブロック方向のパディングの設定

#### HTML

```html live-sample___setting_block_padding_for_vertical_text
<div>
  <p class="exampleText">テキストの例</p>
</div>
```

#### CSS

```css live-sample___setting_block_padding_for_vertical_text
div {
  background-color: yellow;
  width: 120px;
  height: 120px;
}

.exampleText {
  writing-mode: vertical-rl;
  padding-block: 20px 40px;
  background-color: #c8c800;
}
```

#### 結果

{{EmbedLiveSample("Setting_block_padding_for_vertical_text", 140, 140)}}

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- [CSS 論理的プロパティと値](/ja/docs/Web/CSS/CSS_logical_properties_and_values)
- 対応する物理的プロパティ: {{cssxref("padding-top")}}, {{cssxref("padding-right")}}, {{cssxref("padding-bottom")}}, {{cssxref("padding-left")}}
- {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}}
