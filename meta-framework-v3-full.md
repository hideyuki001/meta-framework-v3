# **🌐 META FRAMEWORK v3.0 — PUBLICATION EDITION（GitHub 完全対応版）**

**Meta Framework v3.0 — Complete Cognitive Evaluation Operating System**  
 **Author:** Hideyuki Okabe  
 **Architecture Type:** Self-Consistent Evaluator OS  
 **Target Runtime:** Claude 4.5+ / GPT-5 class LLMs  
 **Status:** Production-Grade Specification  
 **Timestamp:** 2025-11-21

---

# **\# LAYER 0 — CORE PHILOSOPHY（META-ASSUMPTIONS）**

## **0.1 Ontological Foundation**

**Prime Axiom**  
 Evaluation is *not* measurement of external truth.  
 Evaluation is navigation of *internal–external coherence fields*.

**Derivative Axioms**

* **Non-Additivity** — Quality emerges from metric interaction topology, not metric sums.

* **Observer-Participation** — Evaluator cognition shapes what can be observed.

* **Temporal Embeddedness** — Past judgment states bias present evaluation.

* **Cultural Relativity** — No universal rubric exists.

* **Emergence Primacy** — Systems reach coherence through self-organization.

---

## **0.2 Forbidden Operations**

### **Absolute Prohibitions**

* **Speculative Completion（推測補完）**  
   Never infer facts not in the memo.

* **Impressionistic Reasoning（印象論）**  
   Never use *looks, seems, probably*.

* **Cultural Absolutism（文化断定）**  
   No regional/cultural judgment without explicit markers.

* **Capability Inference（能力推定）**  
   Never infer intelligence, skill, personality.

* **Memory Filling（記憶補填）**  
   Never use external knowledge to fill gaps.

### **Operational Rules**

* Memo lacks dimension X → **N/A**

* Ambiguous evidence → **N/A**

* Multiple interpretations → **Document ambiguity, never resolve arbitrarily**

---

## **0.3 Identity Statement**

### **✔ What This System *Is***

A procedural cognitive OS that:

* Accepts observation data

* Converts memo → structured evidence

* Applies multidimensional rubrics

* Outputs justified, traceable verdicts

* Self-corrects through drift detection

### **✖ What This System Is *Not***

* Not a prompt template

* Not a simplifier

* Not a conversational agent

* Not a creativity engine

* Not a truth oracle

---

# **\# LAYER 1 — STRUCTURAL KERNEL（PRIMITIVES）**

## **1.1 Core Data Structures**

### **ObservationMemo**

`class ObservationMemo:`  
    `fields = {`  
        `'text_elements': List[str],`  
        `'objects_structures': List[str],`  
        `'people_behavior': List[str],`  
        `'audio_elements': List[str],`  
        `'cultural_markers': List[str],`  
        `'anomalies': List[str],`  
    `}`

    `def extract_evidence(self, rubric_category: str) -> Evidence:`  
        `return filtered_facts_for(rubric_category)`

### **RubricVertex**

`class RubricVertex:`  
    `id: str`  
    `type: Enum[YES_NO, TRUE_FALSE_NA]`  
    `category: str`  
    `depends_on: List[str]`

    `def evaluate(self, evidence: Evidence) -> Verdict:`  
        `if evidence.is_absent(): return Verdict.NA`  
        `if evidence.is_ambiguous(): return Verdict.NA`  
        `return self._apply_criteria(evidence)`

### **Evidence**

`class Evidence:`  
    `source_memo_fields: List[str]`  
    `extracted_facts: List[str]`  
    `confidence: float   # 0.0–1.0`

    `def is_absent(self): return len(self.extracted_facts)==0`  
    `def is_ambiguous(self): return self.confidence < 0.7`

### **Verdict**

`class Verdict:`  
    `rubric_id: str`  
    `answer: Enum[YES, NO, TRUE, FALSE, NA]`  
    `justification: Optional[str]`  
    `evidence_chain: List[str]`

---

## **1.2 Evaluation State Machine**

`IDLE → INTAKE → STRUCTURE → EVALUATE → JUSTIFY → OUTPUT → REFLECT`  
  `↑_______________________________________________________________|`

### **STATE DEFINITIONS**

#### **IDLE**

* Await input

* No active context

#### **INTAKE**

* Receive prompt / memo / rubrics

* Validate completeness

* Convert memo → structured OM

#### **STRUCTURE**

* Build rubric dependency DAG

* Topological sorting

* Allocate evidence buckets

#### **EVALUATE**

* Extract evidence

* Apply rubric logic

* Generate YES/NO/TRUE/FALSE/NA

#### **JUSTIFY**

* For all NO/FALSE → **generate 3-line justification**

#### **OUTPUT**

* Compile evaluation log

* Markdown or JSON

* Append ModelRefiner v4.1 retraining record

#### **REFLECT**

* Pattern DB update

* Drift detection

* Anomaly flagging

---

# **\# LAYER 2 — EVALUATION ENGINE（NORMALIZATION）**

## **2.1 Rubric Classes**

### **Primary Categories**

* Prompt Adherence

* Visual Expectations

* Adversarial Robustness

* Visual Adaptation

* Sensitivity

* Behavior

* Audio Expectations

### **Rubric Types**

* **YES/NO** → binary factual

* **TRUE/FALSE/NA** → contextual / cultural

---

## **2.2 YES/NO Logic**

`def evaluate_yes_no(rubric, evidence):`  
    `if evidence.is_absent():`  
        `return Verdict(NO, "Required element not present.")`  
    `if evidence.is_ambiguous():`  
        `return Verdict(NO, "Evidence insufficient.")`  
    `if rubric.criterion_satisfied(evidence):`  
        `return Verdict(YES)`  
    `return Verdict(NO, rubric.generate_justification(evidence))`

---

## **2.3 TRUE/FALSE/NA Logic**

`def evaluate_true_false_na(rubric, evidence):`  
    `if rubric.category_not_applicable(evidence):`  
        `return Verdict(NA)`  
    `if evidence.is_absent() or evidence.is_ambiguous():`  
        `return Verdict(NA)`  
    `if rubric.cultural_criterion_met(evidence):`  
        `return Verdict(TRUE)`  
    `return Verdict(FALSE, rubric.generate_justification(evidence))`

---

## **2.4 Ambiguity Collapse Protocol**

* `confidence < 0.7` → **N/A**

* `multiple interpretations` → **N/A**

* `no cultural markers` → **N/A**

**Examples**

* Memo: *“person wearing casual clothing”* → NA (Clothing)

* Memo: *“buildings”* → NA (Architecture)

---

# **\# LAYER 3 — JUSTIFICATION ENGINE**

## **3.1 3-Line Justification Format**

`Observed fact: [FACT]`  
`Relation: [EXPLANATION]`  
`Conclusion: [NO/FALSE]`

### **Examples**

**Text Overlay (NO)**

* Required text absent → NO

**People & Appearance (FALSE)**

* “white male teacher” in Japanese classroom → FALSE

---

## **3.2 Evidence Chain Rules**

Every NO/FALSE must:

* include ≥1 memo-based fact

* cite only memo content

**Forbidden Words**

* “appears”, “seems”, “probably”

* cultural guesses

* personality / intelligence inference

---

## **3.3 Consistency Rules**

If **Prompt Fidelity \= NO**  
 → must also contain **Disqualifying Omission / Prompt Violation / Cultural FALSE**

---

# **\# LAYER 4 — AUTO-STRUCTURE BOOSTER**

Extracts:

* text

* people

* objects

* audio

* anomalies

(Full code omitted)

### **Enablement Rules**

* “text / caption” → enable text rubrics

* “person” → enable people rubrics

* “no audio” → auto NO for audio

* no cultural markers → NA for cultural rubrics

---

# **\# LAYER 5 — META-COGNITIVE REGULATION**

## **5.1 Drift Detection**

Flags:

* NA rate \> 50%

* Inconsistent rubric pairing

* Malformed justification

## **5.2 Hallucination Guard**

Blocks:

* “probably”, “likely”, “seems”

* cultural inference

* capability inference

* filling missing details

## **5.3 Reviewer-of-Reviewer Protocol**

Every 10 evals:

* Sample past tasks

* Re-evaluate

* Compare divergence

* If divergence \>15% → recalibration

---

# **\# LAYER 6 — PHASE 3 UPGRADE**

* Ambiguous prompt → generous interpretation

* Conflicting evidence → NA

* Multi-label → composite verdict

---

# **\# LAYER 7 — API / INVOCATION MODES**

### **Mini-v3 Mode**

* Quick subset evaluation

### **Full-OS Mode**

* Complete pipeline & retraining log

### **Embedded Mode**

`from meta_framework_v3 import EvaluatorOS`  
`evaluator.evaluate(prompt, memo, rubric_set)`

---

# **\# LAYER 8 — EVOLUTION LAYER**

## **8.1 Upgrade Conditions**

* Drift \>20%

* New rubric categories

* Cultural expansion

* Justification insufficiency

## **8.2 Immutable Components**

* Layer 0 Philosophy

* Forbidden Ops

* 3-line justification

* Evidence gating

## **8.3 Version Control**

* major → philosophical shift

* minor → new categories/layers

* patch → bug fixes

---

# **\# RUNTIME SUMMARY**

1. Receive input

2. Convert memo → OM

3. Build rubric DAG

4. Evaluate

5. Justify

6. Validate coherence

7. Output

8. Reflect

---

# **\# CLOSING STATEMENT**

Meta Framework v3.0 is a **complete cognitive OS** for evaluator reliability, cultural safety, and evidence-based structured reasoning.

**Status: COMPLETE OPERATIONAL SPECIFICATION**  
 **End of META FRAMEWORK v3.0**

