# COMASTA Character Plausibility Specification

**Version:** 0.1-draft  
**Status:** Experimental

COMASTA evaluates whether a proposed character behavior can be understood from the character's available conditions.

It does not determine what a character will do.

The current specification is designed for narrative character development, screenwriting, and AI-assisted narrative reasoning.

---

# 1. Assessment Target

Every assessment begins with a proposed behavior.

Example:

`PROPOSED ACTION: The character confronts his father.`

COMASTA evaluates the proposed action against the available character conditions.

The question is:

> Can this behavior be reasonably understood from the available conditions?

The question is NOT:

> Will this character perform this behavior?

---

# 2. Input Domains

COMASTA v0.1 uses the following domains.

## 2.1 History

Known past experiences and behavioral patterns.

Examples:

- previous decisions
- formative experiences
- repeated behavior
- unresolved events
- learned responses

History provides evidence.

History does not determine the future.

---

## 2.2 Relationship

The character's relationship to the people involved in the current event.

Possible dimensions include:

- attachment
- resentment
- dependency
- trust
- fear
- obligation
- unresolved conflict

Opposing relationship states may coexist.

Example:

`attachment: HIGH`  
`resentment: HIGH`

This is not automatically considered inconsistent data.

---

## 2.3 Current State

The character's condition at the moment of action.

Possible dimensions include:

- emotional state
- physical state
- fatigue
- attention
- immediate desire
- immediate fear

Current state must not automatically override history.

History must not automatically override current state.

---

## 2.4 Context

The immediate external situation surrounding the proposed behavior.

Examples:

- location
- presence of other people
- available information
- social circumstances
- immediate opportunity
- environmental constraints

Context can alter which behaviors become plausible.

---

## 2.5 Pressure

Pressure describes conditions that may increase the plausibility of behavioral deviation.

Pressure is not a measurement of the person.

COMASTA v0.1 evaluates pressure using four dimensions:

### Immediacy

How soon must the character respond?

`LOW` — no immediate response is required  
`MEDIUM` — delay has meaningful consequences  
`HIGH` — a decision is required soon  
`EXTREME` — the opportunity or threat is immediate

### Personal Relevance

How strongly does the event involve something important to this character?

`LOW` — peripheral to the character  
`MEDIUM` — personally meaningful  
`HIGH` — connected to an important relationship, value, identity, or desire  
`EXTREME` — connected to something the character experiences as fundamental

### Potential Loss

What may become unavailable or irreversible if the character does not act?

`LOW` — little meaningful loss  
`MEDIUM` — recoverable loss  
`HIGH` — significant or difficult-to-reverse loss  
`EXTREME` — perceived permanent or fundamental loss

### Perceived Control

How much alternative choice does the character believe remains available?

`HIGH` — many alternatives appear available  
`MEDIUM` — alternatives exist but are constrained  
`LOW` — few meaningful alternatives appear available  
`MINIMAL` — the character perceives almost no alternative

---

# 3. Important Rule About Levels

LOW, MEDIUM, HIGH, and EXTREME are ordinal descriptive categories.

They are not claims of objective psychological measurement.

For example:

`pressure: HIGH`

does NOT mean:

`pressure = 80/100`

The level describes the relationship between the event and the known character conditions.

The same event may therefore produce different pressure assessments for different characters.

---

# 4. Baseline Behavioral Tendency

COMASTA may describe an established behavioral tendency.

Example:

`conflict_avoidance: HIGH`

This means the available history strongly supports conflict avoidance as a recurring pattern.

It does NOT mean:

`if conflict → character must avoid`

Behavioral tendencies are evidence, not deterministic instructions.

---

# 5. Support and Conflict

A proposed behavior may contain both supporting and conflicting evidence.

Example:

PROPOSED ACTION:

`Confront father`

Supporting conditions:

- fear of irreversible loss
- unresolved resentment
- high personal relevance
- high immediacy

Conflicting condition:

- long-term conflict avoidance

COMASTA preserves both.

Conflicting evidence must not automatically cancel supporting evidence.

---

# 6. Assessment States

COMASTA v0.1 allows the following assessment states.

## SUPPORTED

The proposed behavior has meaningful support from the available conditions and does not require a major unexplained deviation.

## WEAKLY SUPPORTED

Some conditions support the behavior, but important explanatory gaps remain.

## PLAUSIBLE DEVIATION

The behavior conflicts with an established tendency, but changed conditions provide meaningful support for the deviation.

## CONTRADICTORY BUT PLAUSIBLE

The behavior emerges from conditions that remain internally conflicting, while the action itself can still be understood.

The contradiction does not need to be resolved.

## INSUFFICIENT CONTEXT

The available information is not sufficient to responsibly assess the proposed behavior.

## UNSUPPORTED

The proposed behavior currently lacks meaningful support from the supplied character conditions.

`UNSUPPORTED` does not mean impossible.

It means the current model does not have enough supporting conditions to explain the action.

---

# 7. No Inevitability Rule

No assessment state may imply inevitability.

Therefore:

`SUPPORTED`

does NOT mean:

`WILL HAPPEN`

and:

`UNSUPPORTED`

does NOT mean:

`CANNOT HAPPEN`

COMASTA evaluates interpretive support, not future certainty.

---

# 8. Multiple Valid Behaviors

More than one proposed behavior may receive:

`SUPPORTED`

or:

`PLAUSIBLE DEVIATION`

under the same character conditions.

This is intentional.

The system must not automatically rank one behavior as the character's "true" future action.

---

# 9. Unknown Preservation

The set of behaviors evaluated by COMASTA must not be treated as an exhaustive list of human possibilities.

Even when several plausible behaviors have been identified:

`UNKNOWN`

remains conceptually available.

A character may still act in a way not represented by the current model.

---

# 10. Minimal Assessment Output

A COMASTA-compatible assessment should contain at least:

- proposed behavior
- supporting conditions
- conflicting conditions
- missing information
- assessment state
- explanation
- uncertainty statement

Example:

    Proposed Behavior:
    Confront father

    Supporting Conditions:
    - Potential Loss: HIGH
    - Personal Relevance: HIGH
    - Unresolved Resentment: HIGH

    Conflicting Conditions:
    - Conflict Avoidance: HIGH

    Missing Information:
    - Current emotional state

    Assessment:
    PLAUSIBLE DEVIATION

    Explanation:
    The action conflicts with the character's established avoidance pattern,
    but the possibility of irreversible loss provides meaningful contextual
    support for behavioral deviation.

    Uncertainty:
    This assessment does not imply that confrontation is the character's
    inevitable or most likely action.

---

# 繁體中文

# COMASTA 角色行為成立性規格

**版本：** 0.1-draft  
**狀態：** 實驗中

COMASTA 評估的是：

> 作者提出的某項人物行為，能否從目前已知的人物生命條件中得到理解。

COMASTA 不決定角色將會做什麼。

---

## 1. 評估對象

每一次 COMASTA 評估，都必須先存在一個「提出的行為」。

例如：

`提出行為：角色第一次與父親正面衝突。`

系統詢問：

> 目前條件是否足以讓我們理解這個行為？

而不是：

> 這個角色會不會這樣做？

---

## 2. 基本輸入領域

COMASTA v0.1 暫時使用：

- 歷史 History
- 關係 Relationship
- 當下狀態 Current State
- 情境 Context
- 壓力 Pressure

這些資料共同構成人物當下的條件。

任何單一領域都不應自動取得決定人物行為的權力。

---

## 3. 壓力

壓力不是對人物進行心理數值測量。

COMASTA v0.1 將壓力拆成：

- 迫切性 Immediacy
- 個人關聯 Personal Relevance
- 潛在失去 Potential Loss
- 感知控制 Perceived Control

LOW、MEDIUM、HIGH、EXTREME 是順序性的描述類別，而不是客觀心理分數。

因此：

`HIGH`

不代表：

`80/100`

而是代表目前事件與這個特定人物之間，已經形成高度相關的條件。

---

## 4. 行為傾向不是指令

例如：

`逃避衝突：HIGH`

只代表既有資料高度支持「逃避衝突」是人物反覆出現的行為傾向。

它不代表：

`發生衝突 → 必須逃避`

歷史傾向只能作為理解行為的證據。

---

## 5. 支持與衝突可以共存

同一項行為可以同時具有：

`Supporting Conditions`

以及：

`Conflicting Conditions`

COMASTA 不應為了得到乾淨答案，而自動消除其中一方。

---

## 6. 評估狀態

COMASTA v0.1 暫定六種主要狀態：

`SUPPORTED`

目前條件對該行為具有明確支持。

`WEAKLY SUPPORTED`

存在支持，但仍有重要解釋缺口。

`PLAUSIBLE DEVIATION`

行為偏離人物既有模式，但當下條件足以支持這次偏離。

`CONTRADICTORY BUT PLAUSIBLE`

人物內部條件仍然彼此矛盾，但行為仍可被理解。

`INSUFFICIENT CONTEXT`

資訊不足，不應製造確定答案。

`UNSUPPORTED`

目前資料缺乏足夠條件支持這項行為。

UNSUPPORTED 不代表「人不可能這樣做」。

它只代表：

> 目前提供給系統的資料，還不足以解釋這項行為。

---

## 7. 禁止必然性

任何 COMASTA 評估結果都不得直接等同於未來必然結果。

因此：

`SUPPORTED ≠ WILL HAPPEN`

`UNSUPPORTED ≠ CANNOT HAPPEN`

COMASTA 評估的是理解與成立條件，不是宣判人物未來。

---

## 8. 多重結果

在相同人物條件下，可以同時存在多個：

`SUPPORTED`

或：

`PLAUSIBLE DEVIATION`

這不是系統錯誤，而是設計目的之一。

---

## 9. 保留未知

即使 COMASTA 已經找到多種成立行為，也不應宣稱這些行為已經窮盡人物的所有可能。

因此：

`UNKNOWN`

必須持續保有概念上的位置。

---

## 10. 最小輸出

每次 COMASTA 評估至少應包含：

- 提出的行為
- 支持條件
- 衝突條件
- 缺失資訊
- 評估狀態
- 解釋
- 不確定性聲明

COMASTA 的目的不是找到唯一正確的人物行為。

它的目的，是讓人物行為可以被結構化地理解，同時避免將理解誤認為預測。
