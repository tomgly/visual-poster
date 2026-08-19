# Visual Poster

[![English](https://img.shields.io/badge/lang-English-2f6feb)](README.md)
[![日本語](https://img.shields.io/badge/lang-日本語-6f42c1)](README.ja.md)
[![Styles](https://img.shields.io/badge/styles-9-238636)](sources/00_style_index.md)
[![ChatGPT Project](https://img.shields.io/badge/ChatGPT_Project-ready-10a37f)](PROJECT_INSTRUCTIONS.md)
[![Prompts](https://img.shields.io/badge/prompts-English-555555)](sources/03_prompt_compiler.md)

写真やテーマを、短い指示だけで異なるエディトリアルポスタースタイルへ変換するための再利用可能なプロンプトシステムです。

## スタイル

| # | Style | 特徴 |
|---|---|---|
| 1 | `retro-naive-editorial` | 柔らかなレトロ編集イラストとミックスメディア |
| 2 | `playful-naive-editorial` | ナイーブアート、Bauhaus構成、ファッションスケッチ、遊び心のある視覚表現 |
| 3 | `conceptual-tension-linework` | 緊張、接続、拘束、解放を黒い細線で表現 |
| 4 | `place-narrative-linework` | 場所やテーマの現実的シーンを洗練された線画へ変換 |
| 5 | `storybook-printmaking` | 絵本版画、強い構造面、物語的な色アクセント |
| 6 | `poetic-paper-cover` | 小さな主体、大きな余白、抑制された色、紙の質感 |
| 7 | `observational-field-notes` | 手描き観察ノート、部分図、断片、注釈 |
| 8 | `pastel-impossible-geometry` | 明るいパステル3D、不可能空間、詩的な幾何構成 |
| 9 | `archival-halftone-minimalism` | シルクスクリーン、網点、大きな余白、編集的タイポグラフィ |

詳細は [`sources/00_style_index.md`](sources/00_style_index.md) を参照してください。

## ChatGPT Project のセットアップ

1. ChatGPTで新しいProjectを作成します。
2. [`PROJECT_INSTRUCTIONS.md`](PROJECT_INSTRUCTIONS.md) の内容を **Project Instructions** に貼り付けます。
3. [`sources/`](sources/) 内のMarkdownファイルをすべて **Project Sources** に追加します。
4. 写真をアップロードするかテーマを入力し、スタイルと出力モードを指定します。

`README.md` と `README.ja.md` をProject Sourcesへ追加する必要はありません。

## 使い方

短い指定だけで使えます。

```text
archival-halftone-minimalism, generated only, no text
```

```text
playful-naive-editorial, compare split, minimal text
```

```text
place-narrative-linework
Theme: Yanaka, Tokyo
Mode: compare-split
```

複数スタイルを別々に生成する場合:

```text
Create separate variations using:
- retro-naive-editorial
- poetic-paper-cover
- archival-halftone-minimalism
```

## 出力モード

- `generated-only` — 元画像を参照として使用し、変換後の結果だけを生成。
- `compare-split` — 元画像と変換結果を上下50/50で表示。
- `retouch-only` — 元写真を保持し、写真調整のみを適用。

複数の結果が必要な場合は、コラージュではなく独立したVariationとして扱います。

## ファイル構成

```text
visual-poster/
├── README.md
├── README.ja.md
├── PROJECT_INSTRUCTIONS.md
└── sources/
    ├── 00_style_index.md
    ├── 01_prompt_schema.md
    ├── 02_input_output_modes.md
    ├── 03_prompt_compiler.md
    └── styles/
        ├── 10_retro-naive-editorial.md
        ├── 11_playful-naive-editorial.md
        ├── 12_conceptual-tension-linework.md
        ├── 13_place-narrative-linework.md
        ├── 14_storybook-printmaking.md
        ├── 15_poetic-paper-cover.md
        ├── 16_observational-field-notes.md
        ├── 17_pastel-impossible-geometry.md
        └── 18_archival-halftone-minimalism.md
```
