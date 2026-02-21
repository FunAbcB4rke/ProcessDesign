# CLAUDE.md — ProcessDesign リポジトリガイド

## プロジェクト概要

このリポジトリは**製造業の工程設計（Process Design / Process Planning）**に関するナレッジベースです。製品の設計情報をもとに「どのような工程・設備・方法で製品を製造するか」を計画・設計するための知識を体系的にまとめています。

**対象読者：**
- 製造業の生産技術エンジニア
- 品質保証・品質管理の担当者
- 工程設計をこれから学ぶ方
- APQP / IATF 16949 に関わる方

**言語：** 日本語主体（英語専門用語を括弧内に併記）

---

## リポジトリ構造

```
ProcessDesign/
├── CLAUDE.md          # このファイル
├── README.md          # 記事一覧と概要
└── articles/          # 記事ファイル（15本）
    ├── 01-overview.md
    ├── 02-process-flow-chart.md
    ├── 03-pfmea.md
    ├── 03a-pfmea-absolute-evaluation.md
    ├── 04-control-plan.md
    ├── 05-characteristics-matrix.md
    ├── 06-qc-process-chart.md
    ├── 07-process-instructions.md
    ├── 08-equipment-spec.md
    ├── 09-jig-fixture.md
    ├── 09a-tool-requirement-spec.md
    ├── 09b-tool-requirement-spec-adjustment.md
    ├── 10-floor-plan-layout.md
    ├── 11-packaging-spec.md
    └── 12-process-design-doc.md
```

**注意：** コードファイル・テストファイル・ビルド設定は存在しません。純粋なドキュメントリポジトリです。

---

## 記事の番号体系と依存関係

記事は工程設計の流れに沿って番号付けされています。

```
01-overview.md（全体俯瞰・入口）
  ├── 02-process-flow-chart.md      工程フローチャート
  ├── 03-pfmea.md                   PFMEA（工程FMEA）
  │   └── 03a-pfmea-absolute-evaluation.md  絶対評価法（非自動車向け）
  ├── 04-control-plan.md            コントロールプラン
  ├── 05-characteristics-matrix.md  特性マトリクス
  ├── 06-qc-process-chart.md        QC工程表（日本独自）
  ├── 07-process-instructions.md    作業指示書
  ├── 08-equipment-spec.md          設備仕様書
  ├── 09-jig-fixture.md             治工具設計図
  │   ├── 09a-tool-requirement-spec.md           工具要求仕様書
  │   └── 09b-tool-requirement-spec-adjustment.md 調整・補正工程編
  ├── 10-floor-plan-layout.md       フロアプランレイアウト
  ├── 11-packaging-spec.md          梱包仕様書
  └── 12-process-design-doc.md      工程設計書（総括）
```

`a` / `b` サフィックスは親記事（例：09）のサブトピックを示します。

---

## 各記事の構成パターン

すべての記事は以下の構造に従っています：

1. **はじめに** — 記事の概要・目的
2. **工程設計における位置づけ** — APQP フェーズとの対応
3. **詳細な方法論** — 記事固有のメインコンテンツ
4. **具体例** — インクジェットプリンタ組立を共通事例として使用
5. **よくある問題と解決策**
6. **ベストプラクティス**
7. **参考規格・文献**

---

## 執筆規約

### 言語・表記
- 本文は**日本語**で記述する
- 専門用語（英語）は初出時に括弧内に併記する（例：工程フローチャート（Process Flow Chart））
- 規格名・固有名詞はそのまま表記する（例：APQP、PFMEA、IATF 16949）

### Markdown 記法
- 見出し：`# H1`（記事タイトル）、`## H2`（大見出し）、`### H3`（小見出し）
- 表：GitHub Flavored Markdown（GFM）の表記法
- 構造図・疑似図：バッククォート3つのコードブロック（```）を使用
- 相互参照：相対パスの Markdown リンク（例：`[PFMEA](./03-pfmea.md)`）
- 区切り線：`---` でセクションを区切る

### 記事追加時の手順
1. `articles/` 配下に `NN-topic-name.md` の形式でファイルを作成
2. `README.md` の記事一覧テーブルに追記する
3. 関連する既存記事に相互リンクを追加する

---

## 引用する主要規格・フレームワーク

| 規格 | 用途 |
|------|------|
| APQP 3rd Edition (2024) | 全体フレームワーク（5フェーズ構造） |
| AIAG-VDA FMEA Handbook (2019) | PFMEA の7ステップアプローチ、S/O/D 評価、AP 算出 |
| IATF 16949:2016 | 自動車品質マネジメントシステム要求事項 |
| JIS Z 8206 | 工程フローチャートの記号規格 |
| ISO 9001 | 品質マネジメントシステム（基盤規格） |

---

## 開発ワークフロー

- **ブランチ命名：** `claude/` プレフィックスを使用
- **コミットメッセージ：** 変更内容を端的に記述（日本語または英語）
- **プッシュ：** `git push -u origin <branch-name>`
- **プルリクエスト：** 変更の目的・内容を要約して作成
