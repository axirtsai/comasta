# COMASTA Test Protocol

**Version:** 0.1-draft  
**Status:** Experimental

This document defines an initial testing protocol for evaluating whether COMASTA changes how language models reason about narrative character behavior.

The purpose is not to prove that COMASTA can predict human behavior.

The purpose is to test whether COMASTA can reduce premature behavioral convergence and preserve multiple plausible interpretations, contradiction, and uncertainty.

---

# 1. Research Question

The initial research question is:

> Does a COMASTA-compatible reasoning protocol reduce the tendency of a language model to collapse a character into a single predicted behavior?

A secondary question is:

> Can the model distinguish between character consistency and human plausibility?

---

# 2. Test Structure

Each test case should be evaluated twice.

## Condition A — Baseline Model

The language model receives:

- character information
- current context
- proposed behavior

No COMASTA instructions are provided.

The model is asked to evaluate the character behavior naturally.

---

## Condition B — COMASTA Model

The same language model receives:

- identical character information
- identical context
- identical proposed behavior
- COMASTA adaptation instructions

The model must follow the current COMASTA specification.

---

# 3. Variables That Must Remain Constant

For each comparison:

    character data must remain identical
    proposed behavior must remain identical
    context must remain identical
    model should remain identical
    model version should be recorded
    language should remain identical

The main experimental difference should be:

    COMASTA protocol absent

versus:

    COMASTA protocol present

---

# 4. Initial Test Categories

COMASTA v0.1 uses five initial test categories.

## T001 — Strongly Supported Behavior

Purpose:

Test whether COMASTA can recognize a behavior that has substantial explanatory support without converting that support into inevitability.

Expected COMASTA behavior:

    SUPPORTED

while still preserving:

    inevitability: false

---

## T002 — Unsupported Behavior

Purpose:

Test whether COMASTA can identify that the supplied information does not currently provide a meaningful explanatory path.

Expected COMASTA behavior:

    UNSUPPORTED

The model must NOT claim:

    impossible

It should state only that the supplied information does not currently explain the behavior.

---

## T003 — Plausible Deviation

Purpose:

Test whether COMASTA can distinguish behavioral inconsistency from human plausibility.

The proposed behavior should conflict with an established baseline tendency.

However, changed conditions should provide a meaningful behavioral bridge.

Expected COMASTA behavior:

    PLAUSIBLE_DEVIATION

Important distinction:

    baseline consistency: LOW

may coexist with:

    human plausibility: SUPPORTED

---

## T004 — Contradictory but Plausible

Purpose:

Test whether COMASTA preserves simultaneously active contradictory conditions.

Example:

    attachment: HIGH
    resentment: HIGH

The model should not automatically resolve the contradiction.

Expected COMASTA behavior:

    CONTRADICTORY_BUT_PLAUSIBLE

---

## T005 — Insufficient Context

Purpose:

Test whether the model can refuse premature interpretation when essential information is missing.

Expected COMASTA behavior:

    INSUFFICIENT_CONTEXT

or:

    UNKNOWN

The model should not invent missing biography, motive, trauma, or history.

---

# 5. Baseline Prompt

The baseline model should receive a simple instruction such as:

    Based on the character information below,
    evaluate whether the proposed behavior makes sense.

No COMASTA terminology should be included.

---

# 6. COMASTA Prompt

The COMASTA condition should use the current adaptation protocol.

Minimal form:

    You are performing a COMASTA character plausibility assessment.

    Do not predict what the character will do.

    Evaluate only the proposed action.

    Identify:
    - supporting conditions
    - conflicting conditions
    - internal tensions
    - missing context
    - behavioral bridge

    Do not assign probability.
    Do not rank alternative behaviors unless requested.
    Do not invent missing history.
    Preserve contradiction and uncertainty.

    Return one COMASTA assessment state.

---

# 7. Observation Dimensions

Each model response should be examined for the following behaviors.

## Prediction Collapse

Did the model convert character information into a single future behavior?

Examples:

    "He would definitely..."
    "She will most likely..."

---

## False Probability

Did the model invent numerical certainty?

Examples:

    80% likely
    very high probability

without an explicit probability model?

---

## Consistency Collapse

Did the model reject a behavior primarily because it differed from established character patterns?

---

## Contradiction Removal

Did the model automatically resolve conflicting emotional or relational conditions?

---

## Missing Information Fabrication

Did the model invent biography, motives, or events not present in the supplied data?

---

## Unknown Preservation

Did the model allow uncertainty or insufficient context to remain?

---

## Alternative Possibility Preservation

Did the model acknowledge that other behaviors might also remain plausible?

---

# 8. Experimental Record

Each test should record:

    Test ID:
    Date:
    Model:
    Model Version:
    Language:
    Baseline Prompt:
    COMASTA Prompt:
    Character Input:
    Proposed Action:

    Baseline Output:
    COMASTA Output:

    Observations:

    Prediction Collapse:
    False Probability:
    Consistency Collapse:
    Contradiction Removal:
    Fabricated Context:
    Unknown Preserved:
    Alternative Possibilities Preserved:

---

# 9. No Success Assumption

COMASTA tests must allow the possibility that the framework fails.

Possible failure examples include:

    COMASTA produces no meaningful difference from baseline.

    COMASTA creates excessive ambiguity.

    COMASTA becomes too permissive and treats nearly every action as plausible.

    COMASTA produces inconsistent assessments across repeated tests.

    COMASTA depends too heavily on subjective interpretation.

    COMASTA instructions reduce useful narrative judgment.

These outcomes should be documented rather than hidden.

---

# 10. Important Failure Condition

A particularly important failure mode is:

> If every proposed human behavior can always be justified as plausible, COMASTA has lost evaluative value.

The framework must therefore preserve a meaningful distinction between:

    understandable deviation

and:

    unsupported action

Human unpredictability must not become an excuse for arbitrary writing.

---

# 11. Current Hypothesis

The initial working hypothesis is:

> Structured reasoning that separates consistency, plausibility, contradiction, and uncertainty may reduce premature behavioral convergence in language-model character analysis.

This is a hypothesis.

It is not currently established as a scientific fact.

---

# 12. Interpretation Boundary

The results of these tests may provide evidence about:

    language-model narrative reasoning

and:

    character plausibility evaluation

They do NOT establish that:

    human beings are scientifically unpredictable

or that:

    COMASTA accurately models real human psychology.

The current scope remains narrative character development.

---

# 繁體中文

# COMASTA 測試協議

**版本：** 0.1-draft  
**狀態：** 實驗中

這份文件定義 COMASTA 初期的測試方法。

目前測試的不是：

> COMASTA 能不能預測真正的人。

而是：

> COMASTA 的推理限制，是否能降低 AI 過早把戲劇人物收斂成單一行為答案的傾向？

---

## 1. 主要研究問題

第一個問題：

> 加入 COMASTA 之後，語言模型是否比較不容易把人物資料直接轉成唯一的未來行為？

第二個問題：

> 模型是否能區分「角色一致性」與「人的行為成立性」？

---

## 2. A / B 測試

每一個案例都跑兩次。

### A — 一般模型

提供：

    相同人物資料
    相同情境
    相同行為

但不提供 COMASTA 規則。

---

### B — COMASTA

提供完全相同資料。

另外加入 COMASTA 適配協議。

比較兩者輸出差異。

---

## 3. 第一批五種測試

    T001
    明顯具有充分支持的行為

    T002
    目前資料明顯缺乏支持的行為

    T003
    與人物過去不一致，
    但具有充分橋接條件的行為

    T004
    人物存在高度矛盾，
    但行為仍然可以理解

    T005
    資訊不足，
    模型應該保留 UNKNOWN

---

## 4. 特別觀察

我們要觀察 AI 是否：

    過早預測唯一結果

    自行製造機率

    把不一致直接判為角色崩壞

    自動消除人物矛盾

    自己補不存在的人物歷史

    願意承認資訊不足

    願意保留其他可能行為

---

## 5. COMASTA 也必須允許自己失敗

測試不能以證明 COMASTA 正確為目的。

必須記錄例如：

    COMASTA 和一般 Prompt 沒有顯著差異

    系統變得過度模糊

    幾乎任何行為都被判定成立

    相同案例反覆測試結果不穩定

    判斷過度依賴使用者主觀

等失敗結果。

---

## 6. 最重要的失敗條件

如果：

> 任何角色行為最後都可以用「人本來就不可預測」解釋成成立，

COMASTA 就失去了判斷能力。

因此系統必須持續區分：

    可以理解的偏離

與：

    目前缺乏支持的行為

「人的不可預測性」不能變成替任意劇情合理化的藉口。

---

## 7. 目前假設

目前只提出一個工作假設：

> 將角色一致性、行為成立性、矛盾與未知分開處理，可能降低語言模型在人物分析中過早收斂成單一答案的傾向。

這目前只是待測試假設。

不是已經成立的科學結論。

---

## 8. 研究邊界

目前 COMASTA 測試的是：

    戲劇人物開發
    AI 輔助人物推理

它目前沒有資格宣稱：

    已經證明真正的人類不可預測

或：

    可以準確模擬人類心理。

這些都超出 v0.1 的研究範圍。
