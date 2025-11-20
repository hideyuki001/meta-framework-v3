# Meta Framework v3.0 — Cognitive Evaluation OS  
A procedural, reproducible, and model-agnostic evaluation operating system  
designed by **Hideyuki Okabe** (2025).

---

## 🎯 Overview

**Meta Framework v3.0** は、実務評価ログ（Phase 2/Phase 3 タスクなど）  
40件以上をもとに抽出された「評価者の認知 OS」です。

このフレームワークは、以下を目的として設計されています：

- 推測の排除（Speculative Ban）
- 明確なエビデンスチェーン
- YES/NO と TRUE/FALSE/NA の構造化判断
- 完全再現性（同じメモ → 同じ判定）
- 文化・倫理項目の安全処理  
- Drift（評価揺れ）の検知と抑制
- モデル再学習（ModelRefiner v4.x）との統合

---

## 🧠 Architecture (8-Layer OS)

1. **Layer 0 – Philosophy & Forbidden Operations**  
   推測禁止・文化断定禁止・印象判断禁止などの中核原則。

2. **Layer 1 – Structural Kernel**  
   Observation Memo → Evidence → Verdict の基盤クラス。

3. **Layer 2 – Evaluation Engine**  
   Rubric 正規化、YES/NO ロジック、TRUE/FALSE/NA 判定。

4. **Layer 3 – Justification Engine**  
   3行根拠形式、証拠追跡、禁止推論の抑制。

5. **Layer 4 – Auto-Structure Booster**  
   メモの自然言語 → 構造化変換。

6. **Layer 5 – Meta-Cognitive Regulation**  
   Drift Detection、Consistency Analysis。

7. **Layer 6 – Phase 3 Upgrades**  
   複合ラベル、曖昧プロンプト、自動補正。

8. **Layer 7 – Interface Modes**  
   Mini-v3、Full-OS、Embedding Mode（外部アプリ統合）。

9. **Layer 8 – Evolution Layer**  
   今後の v3.1〜v4.0 進化パス。

---

## 📌 Why v3.0?

- **Uber Phase 2 タスクの評価 OS として最適化**
- 52件のログから「評価者の認知構造」を抽出
- v2 の 45,000字から “実務に必要な核” のみを凝縮
- 文化・倫理項目の安全処理で国際タスクに適合
- Drift（判断揺れ）の自動監視を実装

---

## 🚀 Use Cases

- 評価タスク（Phase 1〜3）
- Safety / RLHF 評価
- 文化・倫理チェック
- 画像・動画の客観評価
- 翻訳 QA（v2 より実務向け）
- ModelRefiner v4.x との併用
- 自作 LLM / エージェントへの組み込み

---

## 📡 Integration

例：Python 実装（疑似コード）

```python
from meta_framework_v3 import EvaluatorOS

evaluator = EvaluatorOS()

result = evaluator.evaluate(
    prompt=user_prompt,
    observation_memo=user_memo,
    rubric_set="phase2_full"
)

print(result.summary)
📈 Status
Version: 3.0

Completion: 96%

Ready for: Production-grade evaluation

Next: v3.1 (Rubric DAG + conflict examples)

📜 License
MIT License (予定）

👤 Author
Hideyuki Okabe
Freelance AI Evaluator / Translation QA Specialist
Developer of ModelRefiner v4.x / Meta Framework v2–3.0
