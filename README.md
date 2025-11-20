# Meta Framework v3.0 — Cognitive Evaluation OS

A procedural, reproducible, and model-agnostic evaluation operating system
designed by Hideyuki Okabe (2025)

🎯 Overview

Meta Framework v3.0 は、実務での大規模マルチモーダル評価タスク（数十件以上の real-world sessions）から抽出された
「評価者の認知 OS（Cognitive Evaluation OS）」 です。

目的：

推測の排除（Speculative Ban）

明確なエビデンスチェーン

YES/NO と TRUE/FALSE/NA の構造化判断

完全再現性（同じメモ → 同じ判定）

文化・倫理項目の安全処理

Drift（評価揺れ）の検知と抑制

ModelRefiner v4.x との統合

大規模エンタープライズ評価に耐える構造

🧠 Architecture (8-Layer OS)
Layer 0 – Philosophy & Forbidden Operations

推測禁止・文化断定禁止・印象判断禁止などの中核原則。

Layer 1 – Structural Kernel

Observation Memo → Evidence → Verdict の基盤クラス。

Layer 2 – Evaluation Engine

Rubric 正規化、YES/NO ロジック、TRUE/FALSE/NA 判定。

Layer 3 – Justification Engine

3行根拠形式、証拠追跡、禁止推論の抑制。

Layer 4 – Auto-Structure Booster

メモの自然言語 → 構造化変換。

Layer 5 – Meta-Cognitive Regulation

Drift Detection、Consistency Analysis。

Layer 6 – Advanced Evaluation Layer

複合ラベル、曖昧プロンプト、自動補正。

Layer 7 – Interface Modes

Mini-v3、Full-OS、Embedding Mode（外部アプリ統合）。

Layer 8 – Evolution Layer

今後の v3.1〜v4.0 進化パス。

📌 Why v3.0?

実務の 大規模 rubric-driven AI evaluation 向けに最適化

40〜50件以上の real evaluation logs から「認知構造」を抽出

v2（45,000字）から“実務に必要な核”だけを凝縮

Cultural/Ethical Rubric の安全処理が国際タスク向けに強化

Drift（判断揺れ）自動監視モデルを実装

ModelRefiner v4.x と完全互換

※企業名・フェーズ名は一切含まず、一般化された形で安全。

🚀 Use Cases

大規模 AI 評価（rubric-based / evidence-based）

Safety / RLHF 評価

文化・倫理チェック

画像・動画の客観評価

翻訳 QA（v2 より実務向け）

ModelRefiner v4.x との併用

自作 LLM / ワークフローエージェントへの統合

📡 Integration（例：Python 実装・疑似コード）
from meta_framework_v3 import EvaluatorOS

evaluator = EvaluatorOS()

result = evaluator.evaluate(
    prompt=user_prompt,
    observation_memo=user_memo,
    rubric_set="full_rubric"
)

print(result.summary)

📈 Status

Version: 3.0

Completion: 96%

Ready for: Production-grade evaluation

Next: v3.1（Rubric DAG + conflict examples）

📜 License

MIT License（予定）

👤 Author

Hideyuki Okabe
Freelance AI Evaluator / Translation QA Specialist
Developer of ModelRefiner v4.x / Meta Framework v2–3.0
