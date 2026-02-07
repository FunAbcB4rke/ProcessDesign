# 製造業における工程設計の全体像

## はじめに

工程設計（Process Design / Process Planning）とは、製品の設計情報をもとに「どのような工程・設備・方法で製品を製造するか」を計画・設計する活動です。製造原価・品質・生産性に直結するため、製造業において極めて重要な役割を担います。

本記事では、工程設計の全体フローを俯瞰し、各段階で作成される**成果物**を一覧化します。個々の成果物の詳細（目的・記載項目・具体例）は別記事で解説します。

---

## 1. 製品開発から量産までの全体フロー

製造業における製品開発から量産までのプロセスは、大きく **5つのフェーズ** に分けられます。これは自動車産業の国際標準である **APQP（Advanced Product Quality Planning / 先行製品品質計画）** のフレームワークに基づいています。

```
Phase 1           Phase 2              Phase 3              Phase 4                 Phase 5
企画・定義   →   製品設計・開発   →   工程設計・開発   →   製品・工程の妥当性確認  →  量産・フィードバック
(Plan & Define)   (Product Design      (Process Design      (Product & Process        (Feedback, Assessment
                   & Development)       & Development)        Validation)               & Corrective Action)
```

各フェーズの終了時には**デザインレビュー（DR）** を実施し、次フェーズへの移行可否を判定します。

| フェーズ | 名称 | 主な活動 |
|----------|------|----------|
| Phase 1 | 企画・定義 | 顧客ニーズの把握、品質・信頼性目標の設定、予備BOMの作成 |
| Phase 2 | 製品設計・開発 | DFMEA作成、試作品の製作・評価、製品図面・仕様書の確定 |
| **Phase 3** | **工程設計・開発** | **工程フロー図、PFMEA、コントロールプラン、作業標準書の作成** |
| Phase 4 | 製品・工程の妥当性確認 | 量産試作、MSA、工程能力調査（Cp/Cpk）、PPAP提出 |
| Phase 5 | 量産・フィードバック | 量産開始、ばらつき低減活動、継続的改善 |

> **補足**: 日本の製造業では、APQPとは別に「企画 → 構想設計 → 詳細設計 → 試作・評価 → 工程設計 → 量産準備 → 量産」という流れが一般的です。本質的な活動はAPQPと共通しています。

---

## 2. 工程設計の成果物一覧

工程設計（Phase 3）およびその前後のフェーズで作成される主要な成果物を以下に示します。

### Phase 3: 工程設計・開発

| # | 成果物 | 英語名 | 主管部門 | 概要 |
|---|--------|--------|----------|------|
| 1 | [工程フロー図](./02-process-flow-diagram.md) | Process Flow Diagram (PFD) | 生産技術 | 受入から出荷までの全工程の流れを図示 |
| 2 | [PFMEA](./03-pfmea.md) | Process FMEA | 生産技術 / 品質 | 各工程の潜在的な故障モードとリスクを分析 |
| 3 | [コントロールプラン](./04-control-plan.md) | Control Plan (CP) | 品質保証 | PFMEAの結果を反映した工程管理計画 |
| 4 | [QC工程表](./05-qc-process-chart.md) | QC Process Chart | 品質保証 | 品質管理の手法・基準を工程ごとに規定 |
| 5 | [作業標準書](./06-work-instruction.md) | Work Instruction (WI) / SOP | 製造 / 生産技術 | 現場作業者向けの具体的な作業手順 |
| 6 | [設備仕様書](./07-equipment-spec.md) | Equipment Specification | 生産技術 | 生産設備の要求仕様を定義 |
| 7 | [治工具設計図](./08-jig-fixture.md) | Jig & Fixture Design Drawing | 生産技術 | 治具・工具・取付具の設計図面 |
| 8 | [工場レイアウト図](./09-plant-layout.md) | Plant Layout Drawing | 生産技術 | 設備配置・物流動線・作業スペースの平面図 |
| 9 | [工程設計書](./10-process-design-doc.md) | Process Design Document | 生産技術 | 工程設計の全体を総括する文書 |

### Phase 4: 製品・工程の妥当性確認

| # | 成果物 | 英語名 | 主管部門 | 概要 |
|---|--------|--------|----------|------|
| 10 | [MSA](./11-msa.md) | Measurement System Analysis | 品質保証 | 測定システムの信頼性を評価 |
| 11 | [工程能力調査](./12-process-capability.md) | Process Capability Study (Cp/Cpk) | 品質保証 | 工程が規格内で安定生産できるかを統計的に評価 |
| 12 | [PPAP / 初品検査](./13-ppap.md) | Production Part Approval Process | 品質保証 | 量産部品が顧客要求を満足することを証明 |

---

## 3. 成果物の依存関係

成果物には明確な**作成順序と依存関係**があります。上流の成果物が下流の成果物のインプットとなります。

```
製品図面・仕様書
    │
    ▼
┌──────────────────────────────────────────────────────────┐
│ Phase 3: 工程設計・開発                                    │
│                                                           │
│   ① 工程フロー図 ─────────────────┐                      │
│       │                            │                      │
│       │                     ⑥ 設備仕様書                  │
│       │                        │                          │
│       │                     ⑦ 治工具設計図                │
│       │                                                   │
│       │                     ⑧ 工場レイアウト図            │
│       ▼                                                   │
│   ② PFMEA（リスク分析）                                   │
│       │                                                   │
│       ▼                                                   │
│   ③ コントロールプラン ←→ ④ QC工程表                     │
│       │                                                   │
│       ▼                                                   │
│   ⑤ 作業標準書                                            │
│       │                                                   │
│   ⑨ 工程設計書（全体の総括文書）                           │
│                                                           │
└──────────────────────────────────────────────────────────┘
    │
    ▼
┌──────────────────────────────────────────────────────────┐
│ Phase 4: 製品・工程の妥当性確認                            │
│                                                           │
│   ⑩ MSA（測定システム解析）                                │
│       │                                                   │
│       ▼                                                   │
│   ⑪ 工程能力調査（Cp/Cpk）                                │
│       │                                                   │
│       ▼                                                   │
│   ⑫ PPAP / 初品検査（量産承認）                            │
│                                                           │
└──────────────────────────────────────────────────────────┘
    │
    ▼
  量産開始
```

### 依存関係のポイント

| 関係 | 説明 |
|------|------|
| 工程フロー図 → PFMEA | 工程フロー図の各ステップに対してリスク分析を行う |
| PFMEA → コントロールプラン | PFMEAで特定した高リスク項目の管理方法を規定する |
| コントロールプラン → 作業標準書 | コントロールプランの管理方法を、現場で実行できる手順に展開する |
| コントロールプラン ↔ QC工程表 | 類似の目的を持つ文書。コントロールプランはIATF 16949で規定された形式、QC工程表は日本独自の慣行 |
| 工程フロー図 → 設備仕様書 | 工程の内容に基づいて必要な設備を定義する |
| 設備仕様書 → 治工具設計図 | 設備に合わせた治工具を設計する |
| 工程フロー図 → 工場レイアウト図 | 工程の流れに基づいて設備配置を計画する |
| MSA → 工程能力調査 | 測定システムの信頼性を確認してから工程能力を評価する |
| 全成果物 → PPAP | PPAPは上記成果物を含む18要素で構成される承認パッケージ |

---

## 4. APQP 5コアツールとの関係

APQP体系では、以下の **5コアツール** が工程設計を支える品質手法として定義されています。

| コアツール | 正式名称 | 工程設計における役割 |
|-----------|---------|----------------------|
| APQP | Advanced Product Quality Planning | 開発全体のプロジェクト管理フレームワーク |
| FMEA | Failure Mode and Effects Analysis | 工程のリスクを事前に分析・低減（PFMEA） |
| SPC | Statistical Process Control | 量産中の工程安定性を管理図で監視 |
| MSA | Measurement System Analysis | 測定の信頼性を保証 |
| PPAP | Production Part Approval Process | 量産部品の顧客承認を取得 |

---

## 5. 用語対訳表

| 日本語 | 英語 | 略称 |
|--------|------|------|
| 工程設計 | Process Design / Process Planning | - |
| 先行製品品質計画 | Advanced Product Quality Planning | APQP |
| 工程フロー図 | Process Flow Diagram | PFD |
| 工程FMEA | Process FMEA | PFMEA |
| コントロールプラン | Control Plan | CP |
| QC工程表 | QC Process Chart | - |
| 作業標準書 | Standard Operating Procedure | SOP |
| 作業手順書 / 作業指示書 | Work Instruction | WI |
| 設備仕様書 | Equipment Specification | - |
| 治工具 | Jig & Fixture | - |
| 工場レイアウト図 | Plant Layout Drawing | - |
| 測定システム解析 | Measurement System Analysis | MSA |
| 工程能力指数 | Process Capability Index | Cp / Cpk |
| 工程性能指数 | Process Performance Index | Pp / Ppk |
| 生産部品承認プロセス | Production Part Approval Process | PPAP |
| 初品検査報告書 | Initial Sample Inspection Report | ISIR |
| 設計部品表 | Engineering Bill of Materials | E-BOM |
| 製造部品表 | Manufacturing Bill of Materials | M-BOM |
| 工程表 | Bill of Process | BOP |
| デザインレビュー | Design Review | DR |
| タクトタイム | Takt Time | - |
| サイクルタイム | Cycle Time | - |
| 歩留まり | Yield Rate | - |
| 統計的工程管理 | Statistical Process Control | SPC |
| 特殊特性 | Special Characteristic | - |
| ポカヨケ | Poka-Yoke (Mistake-Proofing) | - |

---

## 次のステップ

各成果物の詳細記事では、以下の内容を解説します。

- **目的**: なぜその成果物が必要か
- **記載項目**: 何を記載するか
- **作成手順**: どのように作成するか
- **具体例**: テンプレートや記入例
- **よくある課題と対策**: 実務で陥りがちなポイント

---

## 参考規格・文献

- AIAG (Automotive Industry Action Group) - APQP 3rd Edition
- AIAG-VDA FMEA Handbook (2019)
- IATF 16949:2016 - 自動車産業品質マネジメントシステム規格
- JIS Z 8206 - 工程図記号
