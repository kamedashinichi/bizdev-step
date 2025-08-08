# cpf-requirements

## 目的
BtoBtoCモデルのCustomer-Problem Fit（CPF）検証を科学的アプローチで実行し、事業アイデアが真の顧客課題を解決するかをバイアスを排除して検証する。

## 前提条件
- 事業アイデアがBtoBtoCモデル（プラットフォームビジネス）である
- ユーザーから基本情報（事業領域、B側企業、C側消費者、課題仮説）が提供されている
- `/docs/cpf/current/validation/` ディレクトリが存在する（なければ作成）

## 実行内容

1. **初期情報収集**
   - 事業領域の確認
   - プラットフォーム利用企業（B）の特定
   - 最終消費者（C）の特定
   - 両セグメントの課題仮説の整理
   - BtoBtoCモデル特有の前提条件の設定

2. **ペルソナ設定**
   - 企業側詳細ペルソナの作成（デモグラフィック、行動特性、課題）
   - 消費者側詳細ペルソナの作成（デモグラフィック、ライフスタイル、経済行動）
   - 両ペルソナの現実的な設定とバイアス回避

3. **エンパシーマップ作成**
   - 企業側：See/Hear/Think&Feel/Say&Do/Pain/Gainの詳細分析
   - 消費者側：See/Hear/Think&Feel/Say&Do/Pain/Gainの詳細分析
   - 内面的体験の深掘りと課題の本質的理解

4. **カスタマージャーニー作成**
   - 企業側：認知→検討→導入→継続の各段階での体験
   - 消費者側：認知→検討→利用→推奨の各段階での体験
   - BtoBtoCモデル特有の二重の体験フロー設計

5. **仮説生成**
   - 価値提案仮説（企業側・消費者側・プラットフォーム独自価値）
   - ビジネスモデル仮説（収益・チキンエッグ問題・ネットワーク効果）
   - マーケティング仮説（獲得戦略・初期ユーザー獲得順序）

6. **検証用ドキュメント生成**
   - インタビュースクリプトの作成
   - 検証レポートテンプレートの作成
   - 要点サマリースライドの作成

## 出力ファイル

### `/docs/cpf/current/validation/cpf-interview-script.md`
```markdown
# CPF検証インタビュースクリプト
BtoBtoCモデル対応版

## スクリーニング質問
### 企業側スクリーニング質問（4問）
### 消費者側スクリーニング質問（4問）

## 企業向けインタビュースクリプト
### Phase 1-6の詳細スクリプト

## 消費者向けインタビュースクリプト
### Phase 1-6の詳細スクリプト

## 観察ポイント（バイアス回避）
## インタビュー後の記録フォーマット
```

### `/docs/cpf/current/validation/cpf-validation-report.md`
```markdown
# CPF検証統合レポート

## 1. 初期仮説（BtoBtoCモデル）
## 2. 詳細ペルソナ
## 3. エンパシーマップ
## 4. カスタマージャーニー
## 5. インタビュー実施記録
## 6. CPF統合分析
## 7. スコアリング結果
## 8. 改善提案
## 9. 次のステップ
```

### `/docs/cpf/current/validation/cpf-summary-slides.md`
```markdown
---
marp: true
theme: default
paginate: true
title: CPF検証サマリー
---

# CPF検証結果の要点まとめスライド
- 顧客と課題
- 検証結果
- 改善提案
- Next Steps
```

## 機能要件（EARS記法）

### 通常要件
- REQ-001: The system SHALL collect basic business information from the user
- REQ-002: The system SHALL create detailed personas for both B and C segments
- REQ-003: The system SHALL generate empathy maps for both customer segments
- REQ-004: The system SHALL create customer journey maps for BtoBtoC model
- REQ-005: The system SHALL generate multiple hypotheses for value propositions

### 条件付き要件
- REQ-101: WHEN business model is BtoBtoC THEN the system SHALL address chicken-egg problem
- REQ-102: IF insufficient information is provided THEN the system SHALL apply industry best practices
- REQ-103: WHEN creating personas THEN the system SHALL avoid bias and use realistic assumptions

### 制約要件
- REQ-401: The system MUST use scientific approach to avoid confirmation bias
- REQ-402: The system MUST create neutral interview questions
- REQ-403: The system MUST generate practical and actionable interview scripts

## 非機能要件

### 品質要件
- NFR-001: Interview scripts must be neutral and non-leading
- NFR-002: Personas must be realistic and based on market research
- NFR-003: All outputs must be practical and implementable

### ユーザビリティ要件
- NFR-101: All documents must be in structured markdown format
- NFR-102: Files must be organized in logical directory structure
- NFR-103: Content must be accessible to non-technical business users

## 受け入れ基準

### 機能テスト
- [ ] Basic information is correctly collected and processed
- [ ] Detailed personas are created for both segments
- [ ] Empathy maps capture internal experiences accurately
- [ ] Customer journeys reflect BtoBtoC model complexity
- [ ] Multiple hypotheses are generated systematically
- [ ] Interview scripts are comprehensive and neutral
- [ ] All required files are generated in correct locations

### 品質テスト
- [ ] Interview questions are non-leading and neutral
- [ ] Personas are realistic and avoid stereotypes
- [ ] Documents are well-structured and readable
- [ ] Content is actionable and practical
- [ ] BtoBtoC model challenges are properly addressed

## エッジケース

### エラー処理
- EDGE-001: Handle insufficient initial information gracefully
- EDGE-002: Provide default assumptions when specific details are missing
- EDGE-003: Validate BtoBtoC model applicability

### 境界値
- EDGE-101: Handle single-sided platform scenarios
- EDGE-102: Address scenarios with unclear customer segments
- EDGE-103: Handle cases where chicken-egg problem is not applicable

## 成功基準
- All required documentation files are created
- Interview scripts are ready for immediate use
- Personas are detailed and realistic
- Content follows scientific validation principles
- BtoBtoC model considerations are properly integrated