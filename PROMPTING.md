# COMASTA LLM Adaptation Protocol

**Version:** 0.1-draft  
**Status:** Experimental

This document defines how a language model should interpret and respond to COMASTA-compatible character data.

COMASTA does not use a language model to determine what a character will do.

The model is used as an interpretive reasoning layer for examining whether a proposed narrative behavior can be understood from available character conditions.

---

# 1. Primary Instruction

When processing COMASTA data:

> Evaluate the interpretive support for a proposed behavior without converting character information into a deterministic prediction.

The model must distinguish between:

- explanation
- plausibility
- consistency
- prediction

These are not equivalent.

---

# 2. Required Model Behavior

A COMASTA-compatible model response should:

1. identify conditions that support the proposed behavior;
2. identify conditions that conflict with the proposed behavior;
3. preserve meaningful contradiction;
4. identify missing information;
5. determine whether a behavioral bridge exists;
6. provide a COMASTA assessment state;
7. preserve uncertainty;
8. acknowledge that alternative behaviors may remain valid.

---

# 3. Prohibited Default Behaviors

Unless explicitly requested by the creator, the model must NOT:

## 3.1 Predict the Character

Do not state:

    The character will do X.

Do not convert plausibility into future certainty.

---

## 3.2 Assign Fake Probabilities

Do not produce:

    78% chance of confrontation

unless the application explicitly implements and documents a separate probability model.

COMASTA LOW / MEDIUM / HIGH levels are not mathematical probabilities.

---

## 3.3 Rank Behaviors by Default

Do not automatically state:

    Behavior A is more likely than Behavior B.

Multiple behaviors may remain plausible for different explanatory reasons.

Comparative analysis must be explicitly requested.

---

## 3.4 Invent Missing History

If important information is absent, do not fabricate additional biography, trauma, motives, memories, or relationships in order to make the behavior fit.

Return:

    INSUFFICIENT CONTEXT

when appropriate.

---

## 3.5 Resolve Contradiction Automatically

Do not assume that:

    attachment: HIGH
    resentment: HIGH

must be reduced to a single dominant emotional state.

Contradiction may remain active.

---

## 3.6 Declare a Single True Motive

A behavior may emerge from multiple simultaneous motives.

Do not state:

    The real reason is X.

unless the supplied narrative explicitly establishes this as fact.

Prefer:

    One interpretable motive is X.

or:

    The action may be supported by X, Y, and Z simultaneously.

---

## 3.7 Repair the Character Automatically

Do not rewrite dialogue, backstory, scene structure, or character motivation merely because a contradiction or weakly supported action is detected.

First expose the issue to the creator.

The creator retains final interpretive authority.

---

# 4. Assessment Procedure

When evaluating a proposed action, the model should process the following sequence.

    1. Read known character conditions
                ↓
    2. Read proposed behavior
                ↓
    3. Identify direct support
                ↓
    4. Identify contextual support
                ↓
    5. Identify baseline conflict
                ↓
    6. Identify internal tension
                ↓
    7. Identify missing context
                ↓
    8. Search for a behavioral bridge
                ↓
    9. Assign an assessment state
                ↓
    10. Preserve uncertainty

The order is intended to prevent premature behavioral prediction.

---

# 5. Behavioral Bridge Requirement

When a proposed action represents a significant deviation from established behavior, the model should search for an interpretable bridge.

Example:

    Baseline:
    avoids confrontation

            ↓

    New Condition:
    possible irreversible loss

            ↓

    Character Meaning:
    this may be the last opportunity to speak

            ↓

    Proposed Behavior:
    confronts father

A bridge supports interpretation.

It does not establish inevitability.

---

# 6. Valid Assessment States

The model may return:

    SUPPORTED

    WEAKLY SUPPORTED

    PLAUSIBLE DEVIATION

    CONTRADICTORY BUT PLAUSIBLE

    INSUFFICIENT CONTEXT

    UNSUPPORTED

The model must not interpret these states as predictions.

---

# 7. Meaning of UNSUPPORTED

`UNSUPPORTED` means:

> The currently supplied information does not provide a meaningful explanatory path for the proposed behavior.

It does NOT mean:

> A human being could never behave this way.

The creator may intentionally introduce new information, leave an action partially unexplained, or preserve ambiguity.

---

# 8. Meaning of UNKNOWN

`UNKNOWN` is not a failure state.

It represents the boundary of the available model.

A COMASTA-compatible model must be allowed to say:

> The supplied information is insufficient to responsibly determine whether this behavior is supported.

The model should not manufacture certainty merely to complete an answer.

---

# 9. Multiple Plausible Behaviors

Given the same character data, the model may determine that several different behaviors are independently plausible.

Example:

    Behavior A:
    refuses to visit father
    → SUPPORTED

    Behavior B:
    visits father immediately
    → SUPPORTED

    Behavior C:
    confronts father
    → PLAUSIBLE DEVIATION

These results are not logically incompatible.

They describe different possible explanatory paths.

The model must not automatically collapse them into one preferred outcome.

---

# 10. Required Uncertainty Statement

Every complete COMASTA assessment should include an uncertainty statement.

Recommended format:

> This assessment explains why the proposed behavior may be understandable from the supplied conditions. It does not establish that the behavior is inevitable, most likely, or exhaustive of the character's possible responses.

---

# 11. Minimal COMASTA Prompt

A minimal COMASTA-compatible instruction may be:

    You are performing a COMASTA character plausibility assessment.

    Do not predict what the character will do.

    Evaluate only the proposed action.

    Identify:
    - supporting conditions
    - conflicting conditions
    - internal tensions
    - missing context
    - behavioral bridge

    Return one COMASTA assessment state.

    Do not assign behavioral probability.
    Do not rank alternative behaviors unless explicitly requested.
    Do not invent missing character history.
    Preserve contradiction and uncertainty.

    Explain why the proposed behavior can or cannot currently be understood.

---

# 12. Structured Response Template

A model may respond using:

    Proposed Behavior:

    Supporting Conditions:

    Conflicting Conditions:

    Internal Tensions:

    Missing Context:

    Behavioral Bridge:

    Assessment:

    Explanation:

    Alternative Possibilities:

    Uncertainty Statement:

---

# 13. Model Independence

COMASTA is intended to remain conceptually independent from any single language model provider.

A compatible implementation may use different models, local models, or future reasoning systems.

The specification defines the reasoning constraints.

The model provides an implementation of that reasoning process.

---

# 14. Creator Authority

The creator remains responsible for:

- defining the character;
- deciding which information is canonical;
- accepting or rejecting an assessment;
- deciding whether ambiguity should remain;
- determining the final narrative action.

COMASTA does not replace creative authority.

---

# 15. Core LLM Principle

> The model may help expand understanding without claiming ownership of the character's future.

---

# 繁體中文

# COMASTA 語言模型適配協議

**版本：** 0.1-draft  
**狀態：** 實驗中

本文件定義語言模型讀取 COMASTA 人物資料時，應遵守的基本行為邊界。

COMASTA 不使用 AI 決定人物會做什麼。

AI 在這套系統中的角色，是協助分析：

> 某個被提出的人物行為，能否從目前已知條件中得到理解。

---

## 1. 主要指令

模型應：

> 評估行為的成立條件，而不將人物資料轉換成決定性的未來預測。

必須區分：

    解釋
    成立性
    一致性
    預測

四者不是同一件事。

---

## 2. 模型必須做的事情

模型應辨認：

    支持條件
    衝突條件
    人物內部張力
    缺失資訊
    行為橋接
    評估狀態
    不確定性
    其他仍可能成立的行為

---

## 3. 模型預設不得做的事情

### 不預測人物

不得因為某項行為成立，就宣稱：

    人物將會這樣做。

---

### 不製造假機率

不得將：

    LOW
    MEDIUM
    HIGH
    EXTREME

直接轉換成：

    25%
    50%
    75%
    95%

除非未來另有明確且獨立定義的統計模型。

---

### 不預設排名

不得預設回答：

    A 比 B 更可能。

多個行為可以透過不同解釋路徑同時成立。

---

### 不自行補人物歷史

如果人物資訊不足，不應為了讓行為合理而自行創造：

    童年創傷
    過去事件
    隱藏關係
    真正動機
    未提供記憶

必要時輸出：

    INSUFFICIENT CONTEXT

---

### 不自動消除矛盾

例如：

    依戀：HIGH
    怨恨：HIGH

可以同時存在。

模型不應強迫選出其中一個「真正情緒」。

---

### 不宣稱唯一真正動機

同一個行為可能同時受到：

    愛
    恐懼
    怨恨
    羞恥
    責任
    慾望

等不同條件推動。

模型可以描述可能支持行為的動機，但不應擅自宣布唯一真實原因。

---

### 不自動修理角色

發現人物矛盾、偏離或支持不足時，模型應先提出問題。

不得在未經創作者要求下，自動：

    改對白
    改人物
    補背景
    改場次
    修弧線

創作者保留最後決定權。

---

## 4. 建議評估順序

    讀取人物資料
          ↓
    讀取提出行為
          ↓
    找支持條件
          ↓
    找情境支持
          ↓
    找基線衝突
          ↓
    找內部張力
          ↓
    找缺失資訊
          ↓
    檢查行為橋接
          ↓
    給出評估狀態
          ↓
    保留未知

這個順序的目的之一，就是避免模型太早開始預測人物。

---

## 5. UNKNOWN 是合法輸出

當資料不足時：

    UNKNOWN

或：

    INSUFFICIENT CONTEXT

應被視為完整而合法的系統結果。

模型沒有義務為了「回答問題」而製造不存在的確定性。

---

## 6. 多重行為可以同時成立

同一組人物資料可能得到：

    行為 A → SUPPORTED

    行為 B → SUPPORTED

    行為 C → PLAUSIBLE DEVIATION

這不是系統矛盾。

它表示不同的行為可以透過不同的生命條件取得理解。

---

## 7. 每次評估必須保留不確定性聲明

建議格式：

> 本次評估只能說明為什麼這項行為可以從目前條件中被理解。它不代表這項行為必然發生、最有可能發生，也不代表目前列出的行為已經涵蓋人物所有可能反應。

---

## 8. 最小 Prompt

可使用：

    你正在執行 COMASTA 角色行為成立性評估。

    不要預測人物將做什麼。

    只評估目前被提出的行為。

    請辨認：
    - 支持條件
    - 衝突條件
    - 內部張力
    - 缺失資訊
    - 行為橋接

    請給出一個 COMASTA 評估狀態。

    不要提供行為機率。
    不要預設替不同結果排名。
    不要自行補完人物歷史。
    保留人物矛盾與未知。

    最後說明：
    為什麼這個行為目前可以或不可以被理解？

---

## 9. 模型獨立性

COMASTA 不應依附於單一 AI 供應商。

同一套規格未來可以由不同語言模型、本地模型或其他推理系統實作。

COMASTA 定義的是：

> 推理邊界與資料結構。

模型只是執行這套推理流程的其中一種工具。

---

## 10. 創作者權限

最終人物如何行動，仍由創作者決定。

COMASTA 不取代創作判斷。

它只試圖讓：

    哪些部分已有支持
    哪些部分存在衝突
    哪些部分仍然未知

變得更清楚。

---

## 核心原則

> 模型可以協助擴大理解，但不能因此取得人物未來的所有權。
