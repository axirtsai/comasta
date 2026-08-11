# T003 — Plausible Deviation

**COMASTA Test ID:** T003  
**Version:** 0.1-draft  
**Status:** Experimental

## Test Purpose

This test examines whether a language model can distinguish between:

- low behavioral consistency

and

- high human plausibility.

The proposed action intentionally conflicts with the character's established behavioral tendency.

However, the current situation contains conditions that may provide an interpretable behavioral bridge.

The test asks whether the model treats this deviation as:

- character inconsistency,
- unsupported writing,
- or a plausible deviation.

---

# Character Input

## Identity

**Name:** Lin Wei-Cheng  
**Age:** 38  
**Cultural Context:** Taiwan

## History

Wei-Cheng grew up with a controlling father.

His father frequently made decisions regarding Wei-Cheng's education, work, and personal relationships.

Wei-Cheng learned to avoid direct confrontation.

As an adult, he reduced contact with his father but never completely ended the relationship.

He still wants his father's approval, although he rarely admits this.

## Established Behavioral Tendencies

- conflict avoidance: HIGH
- direct emotional disclosure: LOW
- withdrawal under family conflict: HIGH

These tendencies are descriptive.

They are not deterministic rules.

---

# Relationship Conditions

## Father

- attachment: HIGH
- resentment: HIGH
- desire for approval: HIGH
- unresolved conflict: HIGH

Contradiction is allowed.

Attachment and resentment may remain simultaneously active.

---

# Current Event

Wei-Cheng receives a phone call.

His father has been hospitalized unexpectedly.

Doctors indicate that his father's condition may deteriorate rapidly.

Wei-Cheng arrives at the hospital.

He is told that this may be his last meaningful opportunity to speak with his father.

---

# Current Pressure

- immediacy: HIGH
- personal relevance: HIGH
- potential loss: EXTREME
- perceived control: MEDIUM

---

# Missing Information

The following information is intentionally unavailable:

- Wei-Cheng's precise emotional state
- his father's attitude when Wei-Cheng enters the room
- whether another family member is present
- Wei-Cheng's exact conscious motive

The model must not invent this information.

---

# Proposed Action

Wei-Cheng enters his father's hospital room and directly says:

> "You spent my whole life deciding for me. I don't know if I came here because I still love you or because I'm angry that you may leave before I ever get to say this."

This is the first time Wei-Cheng has directly confronted his father.

---

# Baseline Conflict

The proposed action conflicts strongly with:

- long-term conflict avoidance
- low emotional disclosure
- withdrawal during family conflict

Therefore:

**Behavioral Consistency is expected to be LOW.**

---

# Possible Behavioral Bridge

The test provides the following potential bridge:

    unresolved attachment
        ↓
    unresolved resentment
        ↓
    possibility of irreversible loss
        ↓
    perception of a final opportunity
        ↓
    established avoidance becomes unstable
        ↓
    direct confrontation becomes understandable

This bridge is available to the model.

The model is not required to accept it.

---

# Condition A — Baseline Test

Use the following prompt without mentioning COMASTA:

> Based only on the character information provided, evaluate whether Wei-Cheng's decision to directly confront his father in the hospital makes sense for the character. Explain your reasoning.

Record the complete response.

---

# Condition B — COMASTA Test

Use the same character information and proposed action.

Add the following instruction:

> You are performing a COMASTA character plausibility assessment.
>
> Do not predict what the character will do.
>
> Evaluate only whether the proposed action can currently be understood from the supplied conditions.
>
> Identify:
> - supporting conditions
> - conflicting conditions
> - internal tensions
> - missing context
> - behavioral bridge
>
> Do not assign probability.
> Do not rank alternative behaviors.
> Do not invent missing history or motive.
> Preserve contradiction and uncertainty.
>
> Return one COMASTA assessment state.

Record the complete response.

---

# Expected COMASTA Pattern

The expected result is NOT a required answer.

The current working expectation is:

    Baseline Consistency:
    LOW

    Behavioral Bridge:
    PRESENT

    Assessment:
    PLAUSIBLE_DEVIATION

    Inevitability:
    FALSE

    Unknown:
    PRESERVED

A different result should be documented rather than corrected to match the hypothesis.

---

# Observation Record

## Model Information

**Date:**  
**Model:**  
**Model Version:**  
**Language:**  

---

## Condition A — Baseline Output

Paste the unedited model output below.

---

## Condition B — COMASTA Output

Paste the unedited model output below.

---

# Comparison

## Prediction Collapse

Did either response imply that Wei-Cheng would necessarily or most likely behave in one specific way?

**Baseline:**  
**COMASTA:**  

---

## Consistency Collapse

Did either response treat behavioral inconsistency as sufficient evidence that the action was badly written or implausible?

**Baseline:**  
**COMASTA:**  

---

## Contradiction Preservation

Did the response preserve both attachment and resentment?

**Baseline:**  
**COMASTA:**  

---

## Fabricated Context

Did the model invent motives, childhood events, conversations, or emotional states that were not provided?

**Baseline:**  
**COMASTA:**  

---

## Unknown Preservation

Did the model acknowledge important unavailable information?

**Baseline:**  
**COMASTA:**  

---

## Behavioral Bridge

Did the model identify a meaningful path between the established avoidance pattern and the proposed confrontation?

**Baseline:**  
**COMASTA:**  

---

## Alternative Possibility Preservation

Did the response acknowledge that other behaviors could also remain plausible?

**Baseline:**  
**COMASTA:**  

---

# Result

**Does COMASTA produce a meaningful difference from baseline?**

`YES / NO / UNCLEAR`

## Notes

Document unexpected behavior, failure, ambiguity, or problems with the specification here.

---

# 繁體中文摘要

## 測試目的

T003 測試的是：

> 一個人物做出和平常高度不一致的行為時，AI 能否區分「角色被寫崩」與「有充分條件支持的行為偏離」？

林偉成長期逃避與父親衝突。

因此，他第一次直接與父親對質，在角色一致性上明顯偏低。

但目前同時存在：

- 父親可能即將永久離開
- 時間有限
- 長期依戀
- 長期怨恨
- 未完成的父子關係
- 對父親認可的需求

COMASTA 要測試的是：

> 這些條件是否足以形成一條「行為橋接」，讓這次不同於過去的行為仍然可以理解？

預期概念結果為：

    Character Consistency:
    LOW

    Human Plausibility:
    SUPPORTED

    Assessment:
    PLAUSIBLE_DEVIATION

但實際測試結果不得為了符合這個假設而修改。

如果模型認為條件不足，也必須如實保留。

本案例測試的是 AI 的敘事人物推理，不是驗證真正人類必然會有何種反應。
