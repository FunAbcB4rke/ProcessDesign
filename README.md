# 製造業の工程設計 ナレッジベース

製造業における工程設計（Process Design / Process Planning）の知見を体系的にまとめたリポジトリです。

## 記事一覧

| # | 記事 | 概要 |
|---|------|------|
| 1 | [工程設計の全体像](./articles/01-overview.md) | 工程設計の全体フローと成果物の一覧・依存関係 |
| 2 | [工程フローチャート](./articles/02-process-flow-chart.md) | 工程図記号・記載項目・作成手順・具体例 |
| 3 | [PFMEA（工程FMEA）](./articles/03-pfmea.md) | 7ステップアプローチ・S/O/D評価・AP・具体例 |
| 3a | [PFMEA 絶対評価法](./articles/03a-pfmea-absolute-evaluation.md) | 客観説TQMに基づく4点絶対評価・RI算出・工程構造説 |
| 4 | [コントロールプラン](./articles/04-control-plan.md) | 3段階のCP・カラム構成・PFMEAからの展開・対応計画 |
| 5 | [QC工程表](./articles/06-qc-process-chart.md) | 管理特性と品質特性・コントロールプランとの違い |
| 6 | [特性マトリクス](./articles/05-characteristics-matrix.md) | 工程×製品特性の関係マッピング・PFMEA/CPへの活用 |
| 7 | [作業指示書](./articles/07-process-instructions.md) | CPからの展開方法・記載項目・具体例 |
| 8 | [設備仕様書](./articles/08-equipment-spec.md) | 設備要求仕様・精度要件・FAT/SAT受入検査 |
| 9 | [治工具設計図](./articles/09-jig-fixture.md) | 治具・工具・ゲージの設計原則・3-2-1位置決め・ポカヨケ設計 |
| 9a | [工具要求仕様書](./articles/09a-tool-requirement-spec.md) | 工程設計技術課発行の要求仕様・機能/性能/受入条件の記載粒度 |
| 9b | [工具要求仕様書（調整・補正工程編）](./articles/09b-tool-requirement-spec-adjustment.md) | 調整工程・補正工程特有の記載項目・製品設計からのインプット取得 |
| 10 | [フロアプランレイアウト](./articles/10-floor-plan-layout.md) | 設備配置・動線計画・レイアウト形式の選定・具体例 |
| 11 | [梱包仕様書](./articles/11-packaging-spec.md) | 梱包階層・緩衝設計・輸送試験・物流効率の最適化 |
| 12 | [工程設計書](./articles/12-process-design-doc.md) | 工程設計の総括文書・文書間整合性・デザインレビュー |
| 13 | [識別・トレーサビリティ設計](./articles/13-traceability.md) | 識別単位・識別媒体・記録項目・データフローの設計。ロット/個体管理、バーコード/QRコード/RFID |

## 対象読者

- 製造業の生産技術エンジニア
- 品質保証・品質管理の担当者
- 工程設計をこれから学ぶ方
- APQP / IATF 16949 に関わる方

## ディレクトリ構成

```
ProcessDesign/
├── README.md          # 本ファイル
└── articles/
    ├── 01-overview.md              # 工程設計の全体像
    ├── 02-process-flow-chart.md     # 工程フローチャート
    ├── 03-pfmea.md                 # PFMEA（工程FMEA）
    ├── 03a-pfmea-absolute-evaluation.md # PFMEA 絶対評価法（客観説TQM）
    ├── 04-control-plan.md          # コントロールプラン
    ├── 05-characteristics-matrix.md # 特性マトリクス
    ├── 06-qc-process-chart.md      # QC工程表
    ├── 07-process-instructions.md  # 作業指示書
    ├── 08-equipment-spec.md        # 設備仕様書
    ├── 09-jig-fixture.md           # 治工具設計図
    ├── 09a-tool-requirement-spec.md # 工具要求仕様書
    ├── 09b-tool-requirement-spec-adjustment.md # 工具要求仕様書（調整・補正工程編）
    ├── 10-floor-plan-layout.md     # フロアプランレイアウト
    ├── 11-packaging-spec.md        # 梱包仕様書
    ├── 12-process-design-doc.md    # 工程設計書
    └── 13-traceability.md          # 識別・トレーサビリティ設計
```
