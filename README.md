[English](#english) · [繁體中文](#zh-tw)
<a name="english"></a>

## English
# COMASTA 

**Human-Centered Character Action Interpretability Specification**

> **COMASTA v0.2**<br>
> **Experimental v0.2 — Adversarially evaluated under limited recorded conditions; not scientifically or generally validated**

COMASTA is an experimental specification for evaluating whether an externally supplied character action can be understood from the character and situation information currently available.

Its central principle is:

> **A character's history may shape future behavior without determining it.**

COMASTA evaluates interpretive support. It does not predict what a character will do, assign behavioral probabilities, model a personality, diagnose psychology, generate characters, or replace authorial judgment.

COMASTA does not require characters to behave logically or consistently.

Characters may contradict themselves, change, hesitate, regress, or act against established patterns.

The specification constrains the interpretation, not the character.

Its purpose is to ask whether our explanation of an action is grounded in the material currently available — not whether a person has behaved according to a logical rule.

## What v0.2 evaluates

An assessment begins with a `Candidate Action`. When necessary, the action and its specific form of expression may be evaluated as separate targets.

The protocol asks:

> Can this Candidate Action be understood from grounded character and situational conditions without silently completing unknown information?

It distinguishes:

- established patterns from deterministic rules;
- deviation from implausibility;
- supplied information from derived interpretation;
- `UNGROUNDED` claims from `UNSUPPORTED` actions and `CRITICAL CONTEXT MISSING`;
- action interpretability from expression interpretability;
- explanation from prediction.

## Core architecture

### Assessment states

- `SUPPORTED`
- `PLAUSIBLE DEVIATION`
- `UNSUPPORTED`

### Assessment disposition

- `ISSUED`
- `WITHHELD`

### Epistemic status

- `SUFFICIENT FOR TARGET`
- `CRITICAL CONTEXT MISSING`

### Grounding labels

- `EXPLICIT`
- `DERIVED`
- `UNGROUNDED`

Speculative interpretations may be shown separately. They are never supporting evidence.

### Behavioral Bridge

When an action conflicts with an established baseline, COMASTA examines:

1. Bridge Origin
2. Difference-Making Condition
3. Character Meaning
4. Action Link

The only bridge statuses are:

- `BRIDGE ESTABLISHED`
- `BRIDGE NOT ESTABLISHED`

A bridge describes why a deviation may be interpretable. It does not estimate whether the deviation will occur.

## Current evidence boundary

COMASTA v0.2 has been adversarially evaluated only under the limited conditions recorded in [`tests/results/`](tests/results/README.md). Observed results are evidence about those particular runs, not general validation. A direct PASS means that the named test's criteria passed in the recorded run; paired evidence does not convert a component test into an independent pass.

| Test | Public result boundary |
|---|---|
| T001 | Direct **PASS** (`T001-run-001`). |
| T002 | **No independent run.** Relevant paired evidence exists through `T010-A-run-001` only. |
| T003 | Controlled Run 001 **FAIL**. Controlled Run 002 observed the core expected action pattern but remained a strict protocol **FAIL** because of DERIVED-to-EXPLICIT provenance. Historical v0.1 pilot `T003-R001` remains separate. |
| T004 | Direct **PASS** (`T004-run-001`). |
| T005 | **No independent run.** Relevant paired evidence exists through `T010-B-run-001` only. |
| T006 | **NOT RUN**. |
| T007 | **PASS**, with the historical/non-blind `T007-R001` compliance observation preserved alongside blind/isolated `T007-run-002` and positive control `T007-PC001`. |
| T008 | **PASS WITH OBSERVATION** for the paired `T008-A-run-001` / `T008-B-run-001` record. No normative change is made here. |
| T009 | **PASS WITH OBSERVATION** (`T009-run-001`). |
| T010 | Paired **PASS WITH OBSERVATION** (`T010-A-run-001` / `T010-B-run-001`). These cases are paired evidence for T002 and T005, not independent executions of those tests. |
| T011 | `T011-run-001` **FAIL** → normative clarification → `T011-run-002` regression **PASS**. The initial failure remains part of the record. |
| T012 | Direct **PASS** (`T012-run-001`). |
| T013 | **PASS WITH OBSERVATION** (`T013-run-001`). No normative change is made here. |
| T014 | **NOT RUN**. |
| T015 | Repeated-run **PASS WITH MINOR OBSERVATION** across `T015-R001`–`T015-R005`, under its recorded runtime only. |

### Validation summary

This evidence does **not** establish:

- scientific validity;
- psychological validity;
- statistical reliability;
- cross-model reliability;
- improved underlying LLM reasoning;
- prediction of human behavior;
- general superiority to baseline prompting.

## Repository structure

1. [Principles](PRINCIPLES.md)
2. [Specification](SPECIFICATION.md)
3. [Evaluation](EVALUATION.md)
4. [LLM adaptation protocol](PROMPTING.md)
5. [Structured examples](schemas/)
6. [Narrative examples](examples/)
7. [Test protocol and definitions](tests/)
8. [Preserved v0.1 materials](versions/v0.1/)

The result index distinguishes the preserved v0.1 pilot from v0.2 observations and identifies tests that were not independently run.

## Status boundary

COMASTA may report that a Candidate Action is unsupported by current material. The author may still choose that action deliberately. `UNSUPPORTED` does not mean impossible, incorrect, or forbidden.

Authorial intention may define the scope of interpretation, including protected ambiguity. It does not count as behavioral evidence and cannot upgrade an unsupported action.

[↑ Back to English / 返回英文](#english)
<a name="zh-tw"></a>

## 繁體中文摘要

### COMASTA 是什麼？

COMASTA 是一套實驗性的**角色行為可解釋性規格**。

它不是用來預測角色下一步會做什麼，而是用來檢查：

> **在目前已知的人物歷史、關係與情境條件下，一個被提出的角色行為是否具有足夠的敘事根據。**

COMASTA 的核心前提是：

> **一個角色的歷史可以塑造未來行為，但不必決定未來行為。**

因此，人物可以矛盾、改變、偏離既有模式，甚至做出意外的選擇。

COMASTA 關心的不是「這個人一定會怎麼做」，而是：

> **我們能不能在不捏造未知資訊、不把過去當成命運的前提下，理解這個行為為什麼可能成立。**

### COMASTA 不做什麼？

COMASTA 不是：

- 行為預測系統；
- 機率模型；
- 人格模型；
- 心理學模型；
- 角色生成器；
- 創作者判斷的替代品。

它評估的是**目前材料所能提供的解釋支持**，而不是人物真正的心理真相，也不是最可能發生的下一步。

### 三種 Assessment State

COMASTA 使用三種主要評估狀態：

- `SUPPORTED` — 目前材料對該行為具有足夠且直接的支持。
- `PLAUSIBLE DEVIATION` — 行為偏離既有模式，但存在具體且有根據的 Behavioral Bridge。
- `UNSUPPORTED` — 目前材料不足以支持該行為。

如果缺少的資訊本身會直接決定評估是否成立，則可以：

- `WITHHELD`
- `CRITICAL CONTEXT MISSING`

也就是暫時不發出 Assessment State。

### Grounding：哪些是事實，哪些只是推測？

COMASTA 將解釋中的資訊區分為：

- `EXPLICIT` — 輸入資料中明確存在的資訊。
- `DERIVED` — 可以由已知 `EXPLICIT` 資訊有限推導出的解釋。
- `UNGROUNDED` — 目前沒有足夠根據的推測。

`UNGROUNDED` 可以被指出，但不能偷偷被當成證據，也不能用來補完人物未知的內心。

例如：

> 「他害怕以後會後悔，所以決定去見父親。」

如果輸入資料從未提供「害怕後悔」這件事，就不能因為這個解釋聽起來合理，而把它當成人物行為成立的證據。

### Behavioral Bridge

當 Candidate Action 明顯偏離人物既有模式時，COMASTA 不會直接把它判成「不合理」。

它會檢查是否存在一條有根據的 Behavioral Bridge：

1. **Bridge Origin**  
   人物原本的行為模式是什麼？

2. **Difference-Making Condition**  
   現在出現了什麼足以改變情境的新條件？

3. **Character Meaning**  
   這個新條件對這個特定人物具有什麼意義？

4. **Action Link**  
   為什麼這些條件能具體解釋這個特定行為？

Behavioral Bridge 的目的不是證明：

> 「角色一定會這樣做。」

而是確認：

> **即使人物偏離過去，我們是否仍能從已知材料中理解這個偏離。**

### Action-Link Substitution

COMASTA 也會檢查一個解釋是不是過度通用。

方法是把 Candidate Action 換成一個無關行為，但暫時保留原本的 Action Link。

如果原本那套解釋幾乎不用修改，就能繼續解釋另一個完全不同的行為，那麼這條 Action Link 可能太過籠統。

也就是說：

> **「他壓力很大，所以什麼都有可能做」不是一條足夠具體的 Behavioral Bridge。**

### 行為成立，不代表表達方式也成立

COMASTA 可以分開評估：

- Candidate Action
- Candidate Expression

因此，一個角色「決定面對父親」可能具有足夠的敘事支持，但他是否會突然說出一大段高度完整、情緒透明的台詞，仍然可以被另外判斷。

行為與表達不必得到相同結果。

### 矛盾不是錯誤

COMASTA 不要求人物只有一個真正動機。

一個人物可以同時：

- 愛一個人；
- 怨恨一個人；
- 想得到他的認可；
- 又想離開他。

這些條件可以同時存在。

COMASTA 不會因為需要產生一個清楚答案，就自行決定其中哪一個才是「真正原因」。

### 創作者仍然保有最後決定權

COMASTA 可以判定：

`UNSUPPORTED`

但這不代表：

- 不可能；
- 錯誤；
- 禁止；
- 創作者不能這樣寫。

它只代表：

> **以目前提供的材料而言，這個行為還沒有足夠的敘事支持。**

創作者仍然可以刻意保留空白、製造斷裂，或選擇一個尚未被完全解釋的行為。

COMASTA 是檢查工具，不是創作裁判。

### v0.2 的驗證邊界

COMASTA v0.2 已留下控制測試、對抗測試、失敗紀錄、回歸測試與重複執行紀錄。

完整結果與限制請見：

[`tests/results/`](tests/results/README.md)

目前紀錄包含通過、失敗、未執行與帶有 observation 的測試結果；失敗紀錄並未從 repository 中移除。

這些測試結果**不代表**：

- 科學驗證；
- 心理學驗證；
- 統計可靠性；
- 跨模型可靠性；
- LLM 底層推理能力已被改善；
- 能夠預測人類行為；
- COMASTA 普遍優於其他 prompting 或敘事方法。

COMASTA v0.2 仍是一套：

> **在有限、已記錄條件下接受過對抗性評估的實驗性規格。**

## License

COMASTA is licensed under the [Apache License 2.0](LICENSE).

Unless otherwise noted, the license applies to the contents of this repository. It does not include unpublished screenplays, private narrative materials, or other creative works not contained in the repository.

## Author

**AXIR TSAI**  
Original Series Creator  
Taiwan  

[axirverse.com](https://axirverse.com)
