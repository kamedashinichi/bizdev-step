# psf-requirements

## 目的
CPF検証で80点以上を獲得した顧客課題に対し、提案するソリューションがBtoBtoCモデルで真に価値を提供し、両セグメントの顧客に受け入れられるかを科学的アプローチで検証する。

## 前提条件
- CPF検証が完了し、企業側・消費者側共に80点以上のスコアを獲得済み
- 顧客課題が明確に特定され、詳細ペルソナが作成されている
- `/docs/cpf/current/validation/` ディレクトリにCPF検証結果が存在する
- BtoBtoCプラットフォームモデルが適用される

## 実行内容

1. **CPF結果の継承**
   - CPF検証で特定された企業側・消費者側ペルソナ（各5名）の継続
   - 検証済み顧客課題の詳細分析
   - BtoBtoCモデル特有の課題（チキンエッグ問題等）の考慮

2. **ソリューション仮説構築**
   - 企業向けソリューション機能の詳細設計
   - 消費者向けソリューション機能の詳細設計
   - プラットフォーム全体価値提案の定義
   - 技術的実現可能性の評価

3. **PSF検証スクリプト作成**
   - 企業側・消費者側スクリーニング設問（各4問）
   - 企業向けPSFインタビュースクリプト（4フェーズ構成）
   - 消費者向けPSFインタビュースクリプト（4フェーズ構成）
   - バイアス回避のための中立的質問設計

4. **インタビュー実施シミュレーション**
   - CPFから継続する企業側対象者5名との検証
   - CPFから継続する消費者側対象者5名との検証
   - 現実的な反応分布（肯定30%、中立40%、否定30%）
   - 導入障壁と価格感度の詳細分析

5. **統合分析とスコアリング**
   - 企業側・消費者側PSFスコア算出（各100点満点）
   - BtoBtoCプラットフォーム統合評価
   - 競合優位性分析と差別化ポイント特定
   - MVP機能要件の優先順位付け

6. **V0プロトタイプ設計**
   - 検証結果に基づくペルソナ別UI設計
   - 導入障壁を解決するUX要素の組み込み
   - V0.dev用プロトタイプデモ設計プロンプト作成
   - 投資家・顧客提示用デモ戦略策定

## 出力ファイル

### `/docs/psf/current/validation/psf-validation-report.md`
```markdown
# PSF検証統合レポート

## 1. BtoBtoCソリューション仮説
### プラットフォーム全体価値提案
### 企業向けソリューション機能
### 消費者向けソリューション機能
### 技術的実現可能性

## 2. PSF検証対象者プロフィール
### 企業側対象者（CPFから継続・5名）
### 消費者側対象者（CPFから継続・5名）

## 3. インタビュー実施記録
### 企業側インタビュー結果
### 消費者側インタビュー結果

## 4. PSF統合分析
### ソリューション評価集計
### 導入障壁分析
### 価格戦略の示唆
### PSFスコアリング結果

## 5. MVP定義とロードマップ
## 6. 次のアクション
```

### `/docs/psf/current/validation/psf-interview-script.md`
```markdown
# PSFインタビュースクリプト
BtoBtoCモデル対応版

## スクリーニング質問
### 企業側スクリーニング質問（4問）
### 消費者側スクリーニング質問（4問）

## 企業向けPSFインタビュースクリプト
### Phase 1-4の詳細スクリプト

## 消費者向けPSFインタビュースクリプト
### Phase 1-4の詳細スクリプト

## インタビュー実施記録テンプレート
```

### `/docs/psf/current/validation/psf-summary-slides.md`
```markdown
---
marp: true
theme: default
paginate: true
title: PSF検証サマリー
description: Problem-Solution Fit検証結果の要点まとめ
---

# PSF検証結果の要点まとめスライド
- 課題と解決策
- 検証結果スコア
- 企業側・消費者側フィードバック
- 導入障壁と対策
- MVP定義
- Next Steps
```

### `/docs/psf/prototype/v0-prompt.md`
```markdown
# V0プロトタイプデモ設計プロンプト

## プロダクト概要
## ペルソナ別UI設計（企業5パターン・消費者5パターン）
## 統合BtoBtoC接続インターフェース
## 導入障壁対策UX要素
## 技術要件
```

## 機能要件（EARS記法）

### 通常要件
- REQ-001: The system SHALL inherit validated customer personas from CPF phase
- REQ-002: The system SHALL create detailed solution hypotheses for both B and C segments
- REQ-003: The system SHALL generate screening questions for PSF interviews
- REQ-004: The system SHALL conduct simulated PSF interviews with realistic response distribution
- REQ-005: The system SHALL calculate PSF scores for both segments using standardized criteria
- REQ-006: The system SHALL create V0 prototype design prompt based on validation results

### 条件付き要件
- REQ-101: WHEN CPF score is below 80 for any segment THEN the system SHALL not proceed to PSF
- REQ-102: IF technical feasibility is questioned THEN the system SHALL provide alternative approaches
- REQ-103: WHEN pricing sensitivity is high THEN the system SHALL explore freemium models

### 状態要件
- REQ-201: WHERE BtoBtoC chicken-egg problem exists the system SHALL propose staged rollout strategies
- REQ-202: WHERE competitive landscape is crowded the system SHALL identify differentiation opportunities

### 制約要件
- REQ-401: The system MUST maintain scientific neutrality in interview simulations
- REQ-402: The system MUST address BtoBtoC platform-specific challenges
- REQ-403: The system MUST create realistic and implementable prototype designs

## 非機能要件

### 品質要件
- NFR-001: Interview scripts must be neutral and avoid confirmation bias
- NFR-002: Solution hypotheses must be technically feasible and scalable
- NFR-003: PSF scoring must be objective and based on clear criteria
- NFR-004: V0 prototype designs must address identified adoption barriers

### ユーザビリティ要件
- NFR-101: All documents must follow consistent markdown structure
- NFR-102: Prototype designs must be implementable in V0.dev
- NFR-103: Content must be investor and stakeholder friendly

### 実装要件
- NFR-201: PSF validation must build upon CPF results
- NFR-202: All outputs must support decision-making for next phase
- NFR-203: Documentation must enable handoff to development team

## 受け入れ基準

### 機能テスト
- [ ] CPF results are properly inherited and analyzed
- [ ] Solution hypotheses address validated customer problems
- [ ] Screening questions effectively filter target users
- [ ] PSF interviews simulate realistic user responses
- [ ] Scoring methodology is consistent and objective
- [ ] V0 prototype design addresses adoption barriers
- [ ] All required output files are generated

### 品質テスト
- [ ] Interview questions are neutral and non-leading
- [ ] Solution features map directly to customer problems
- [ ] Technical feasibility is realistically assessed
- [ ] Pricing strategies reflect market sensitivity
- [ ] Prototype designs are user-centric and implementable
- [ ] Documentation supports investment and development decisions

## エッジケース

### エラー処理
- EDGE-001: Handle cases where CPF personas need refinement for PSF
- EDGE-002: Address scenarios where solution complexity exceeds MVP scope
- EDGE-003: Manage situations where B and C segment needs conflict

### 境界値
- EDGE-101: Handle split decisions where one segment scores high, other low
- EDGE-102: Address cases where technical feasibility is marginal
- EDGE-103: Manage scenarios where competitive landscape changes during validation

## PSFスコアリング基準（100点満点）

### 企業側PSFスコア
1. **課題解決の的確性（25点）**
   - 特定課題への直接的解決度
   - 根本原因への対処度
   - 期待効果の実現可能性

2. **ソリューションの受容性（25点）**
   - 使いやすさとlearning curve
   - 既存ワークフローへの適合性
   - 導入障壁の低さ

3. **競合優位性（25点）**
   - 既存解決策に対する優位性
   - 差別化ポイントの明確性
   - 競合対抗の困難度

4. **実装可能性（25点）**
   - 技術的実現可能性
   - 予算・リソース適合性
   - 導入タイムラインの現実性

### 消費者側PSFスコア
同様の4基準で評価、ただし消費者特有の要素を考慮：
- 操作の直感性
- 価格感度
- プライバシー懸念
- ネットワーク効果への期待

### BtoBtoCプラットフォーム統合評価
- 両セグメント平均スコア
- チキンエッグ問題への対処度
- ネットワーク効果の実現可能性
- 収益モデルの持続可能性

## 成功基準
- 企業側PSFスコア：80点以上でビジネスモデル構築へ
- 消費者側PSFスコア：80点以上でビジネスモデル構築へ
- 統合評価：全スコア帯でまずV0デモ作成、フィードバック後判定
- V0デモ評価：高評価でビジネスモデル構築、要改善で再検証

## V0プロトタイプ要件
- PSF検証で特定された10名のペルソナ別インターフェース
- 導入障壁を解決するUX要素の具体的実装
- BtoBtoC統合価値の視覚的表現
- 投資家・顧客への説得力のあるデモ構成
- V0.devで実装可能な技術仕様