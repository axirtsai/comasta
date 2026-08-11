# COMASTA Evaluation Model

**Version:** 0.1-draft  
**Status:** Experimental

COMASTA does not calculate human plausibility by adding psychological scores.

It evaluates whether a proposed behavior has a coherent explanatory path through the known conditions surrounding a character.

The purpose is not to calculate the most likely behavior.

The purpose is to determine whether a proposed behavior can currently be understood without treating that behavior as inevitable.

---

# 1. Non-Additive Evaluation

COMASTA does not use a rule such as:

    HIGH + HIGH + MEDIUM = SUPPORTED

Human conditions must not be treated as interchangeable numerical units.

For example:

    Attachment: HIGH
    Resentment: HIGH

does not equal:

    Emotional State: 0

Both conditions may remain active simultaneously.

Their coexistence may be important to understanding the behavior.

Therefore:

> Human contradiction must not be mathematically cancelled.

---

# 2. Evidence Is Relational

A condition only becomes meaningful when connected to a proposed behavior.

Example:

    Condition:
    Fear of abandonment

This condition has no fixed behavioral meaning.

It may support:

- staying in a relationship
- leaving before being abandoned
- becoming controlling
- remaining silent
- seeking reassurance
- avoiding intimacy

Therefore COMASTA does not ask:

> What behavior does this trait produce?

It asks:

> How does this condition support or conflict with this proposed behavior under the current situation?

---

# 3. Evaluation Objects

For every proposed behavior, COMASTA identifies five possible evidence roles.

## 3.1 Direct Support

A known condition provides a clear explanatory connection to the proposed behavior.

Example:

    Proposed behavior:
    Goes to hospital

    Direct support:
    Fear of losing father permanently

---

## 3.2 Contextual Support

A current circumstance changes the meaning or plausibility of an action.

Example:

    Father's condition may become irreversible tonight.

This condition does not define the character.

It changes the decision environment.

---

## 3.3 Baseline Conflict

The proposed behavior conflicts with an established behavioral tendency.

Example:

    Baseline:
    Avoids confrontation

    Proposed behavior:
    Confronts father

Baseline conflict must be preserved rather than automatically treated as failure.

---

## 3.4 Internal Tension

Two or more meaningful conditions pull the character in different directions.

Example:

    Attachment: HIGH
    Resentment: HIGH

This should be represented as tension.

It should not automatically be resolved.

---

## 3.5 Missing Context

Important information required for responsible interpretation is unavailable.

Example:

    Current emotional state: UNKNOWN

Missing context may reduce confidence in an assessment.

In some cases it should prevent assessment entirely.

---

# 4. Explanatory Path

A proposed behavior becomes meaningfully supported when COMASTA can identify an explanatory path connecting known conditions to the action.

Example:

    Long-term attachment
        ↓
    Possibility of irreversible loss
        ↓
    Increased urgency
        ↓
    Temporary override of avoidance pattern
        ↓
    Goes to hospital

This path does NOT mean:

    The character must go to the hospital.

It means:

    If the character goes to the hospital,
    the available conditions provide a coherent way to understand that action.

---

# 5. Behavioral Deviation

Behavioral deviation occurs when a proposed action conflicts with a known baseline tendency.

Deviation is not automatically implausible.

COMASTA evaluates whether changed conditions provide a meaningful bridge between the baseline and the proposed behavior.

Example:

    Baseline:
    Avoids confrontation

        ↓

    Changed Condition:
    Father's possible imminent death

        ↓

    Character Meaning:
    Last opportunity to speak

        ↓

    Proposed Behavior:
    Direct confrontation

If this bridge can be articulated, the behavior may be classified as:

    PLAUSIBLE DEVIATION

---

# 6. The Bridge Requirement

A major behavioral deviation should not be justified only by saying:

    "People are unpredictable."

Unpredictability is not sufficient explanation.

For a deviation to be meaningfully supported, COMASTA should identify at least one interpretable bridge between:

    established character conditions

and:

    proposed behavior

A bridge may arise from:

- changed pressure
- changed relationship conditions
- new information
- perceived irreversible loss
- immediate threat
- accumulated tension
- changed self-perception
- altered social context
- physical condition
- a newly available opportunity
- another explicitly defined condition

The bridge does not need to eliminate contradiction.

It only needs to make the deviation intelligible.

---

# 7. Sufficient Support

COMASTA does not define sufficient support by counting conditions.

Instead, support is considered sufficient when:

1. the proposed behavior has at least one interpretable explanatory path;
2. the relevant conditions meaningfully connect to the action;
3. major conflicts are acknowledged rather than hidden;
4. no critical missing information makes the interpretation irresponsible;
5. the explanation does not require declaring the behavior inevitable.

This remains an interpretive assessment.

COMASTA does not claim that this process produces objective psychological truth.

---

# 8. Assessment Logic

## SUPPORTED

Use when:

- an explanatory path is clear;
- the behavior does not require a major unexplained departure from established patterns;
- important conflicting conditions are accounted for.

---

## WEAKLY SUPPORTED

Use when:

- some explanatory support exists;
- but important links remain unclear;
- or important missing context prevents a stronger interpretation.

---

## PLAUSIBLE DEVIATION

Use when:

- the behavior conflicts with an established tendency;
- a meaningful bridge explains why deviation has become understandable;
- the deviation remains non-inevitable.

---

## CONTRADICTORY BUT PLAUSIBLE

Use when:

- important conditions actively pull in opposing directions;
- the contradiction remains unresolved;
- the proposed behavior can still be meaningfully understood within that tension.

---

## INSUFFICIENT CONTEXT

Use when:

- critical information required for meaningful interpretation is missing;
- generating a confident explanation would require inventing unsupported assumptions.

---

## UNSUPPORTED

Use when:

- no meaningful explanatory path currently connects the available conditions to the proposed behavior.

UNSUPPORTED means:

> not currently explained by the model.

It does NOT mean:

> impossible for a human being.

---

# 9. No Automatic Ranking

COMASTA should not automatically conclude:

    Behavior A > Behavior B > Behavior C

unless a specific application explicitly requests comparative analysis.

Multiple behaviors may remain equally interpretable for different reasons.

The default purpose is possibility analysis, not behavioral prediction.

---

# 10. No Automatic Repair

When COMASTA detects:

- contradiction
- behavioral deviation
- missing context
- weak support

it should not automatically rewrite the character or scene.

The system should first expose the condition to the creator.

Example:

    Warning:
    This action represents a major deviation from the established pattern.

    Current bridge:
    Irreversible loss + high relational relevance.

    Missing:
    Current emotional state.

    Suggested question:
    Does the creator intend this deviation to remain partially unexplained?

The creator retains interpretive authority.

---

# 11. Unknown Preservation

Even a strong explanatory path does not exhaust the character.

Therefore every assessment remains bounded by:

    KNOWN CONDITIONS
    ≠
    TOTAL HUMAN POSSIBILITY

COMASTA may describe what is currently understandable.

It must not claim to contain the entire person.

---

# 12. Core Evaluation Principle

> The stronger the model becomes, the more precisely it should distinguish between what can be understood, what remains unsupported, and what must remain unknown.

---

# 繁體中文

# COMASTA 評估模型

**版本：** 0.1-draft  
**狀態：** 實驗中

COMASTA 不透過加總心理數值來計算人物是否成立。

它評估的是：

> 一項被提出的人物行為，能否透過目前已知的人物條件形成一條可以理解的解釋路徑。

系統不是計算：

> 哪一種行為最可能發生？

而是檢查：

> 如果人物做了這件事，我們目前是否有足夠條件理解它？

---

## 1. 非加總式評估

COMASTA 不採用：

    HIGH + HIGH + MEDIUM = SUPPORTED

這類判定方式。

人物條件不是可以彼此兌換的數值單位。

例如：

    依戀：HIGH
    怨恨：HIGH

不能被計算成：

    情緒：0

兩者可以同時存在。

而且兩者同時存在，本身可能正是理解人物的關鍵。

因此：

> 人的矛盾不能被數學抵銷。

---

## 2. 條件沒有固定行為答案

例如：

    害怕被拋棄

不能直接推出某一種行為。

它可能支持：

- 留在關係裡
- 先主動離開
- 控制對方
- 沉默
- 不斷確認感情
- 避免建立親密關係

因此 COMASTA 不問：

> 這種人格會做什麼？

而問：

> 在目前情境下，這項條件如何支持或衝突於這個被提出的行為？

---

## 3. 五種證據角色

COMASTA 暫時將條件分成五種作用：

### 直接支持 Direct Support

條件和行為之間存在明確的理解關係。

### 情境支持 Contextual Support

當下環境改變了某項行為的成立程度。

### 基線衝突 Baseline Conflict

提出的行為與人物過去的主要行為傾向衝突。

### 內部張力 Internal Tension

人物同時存在彼此拉扯的條件。

### 缺失資訊 Missing Context

目前缺少對判斷具有重要影響的資料。

---

## 4. 解釋路徑

例如：

    長期依戀
        ↓
    父親可能永久離開
        ↓
    時間突然變得有限
        ↓
    原本逃避模式受到挑戰
        ↓
    前往醫院

這不代表：

    他一定會去醫院。

它只代表：

> 如果作者讓他去醫院，目前存在一條足以理解這個行為的路徑。

---

## 5. 行為偏離

人物做出和平常不同的事情，不應自動被判定為角色崩壞。

COMASTA 必須尋找：

    既有行為模式
        ↓
    發生了什麼變化？
        ↓
    這個變化對人物代表什麼？
        ↓
    新行為

這個中間連結稱為：

**Behavioral Bridge / 行為橋接**

---

## 6. 行為橋接原則

重大偏離不能只用：

> 人本來就不可預測。

來合理化。

「人不可預測」不等於任何行為都可以成立。

必須至少存在一項可理解的橋接條件，例如：

- 壓力改變
- 關係改變
- 新資訊
- 不可逆失去
- 立即威脅
- 長期張力累積
- 自我認知改變
- 社會情境改變
- 身體狀態
- 突然出現的新選擇

橋接不需要消除矛盾。

它只需要使偏離變得可以理解。

---

## 7. 什麼叫足夠支持？

COMASTA 不透過計算 HIGH 的數量決定。

暫時定義為：

1. 行為至少存在一條可以理解的解釋路徑；
2. 支持條件與行為之間存在實質關係；
3. 主要衝突被保留並說明；
4. 沒有關鍵資訊缺失到使判斷變得不負責任；
5. 解釋過程不需要宣稱行為必然發生。

這仍然是一種敘事與人文判斷。

COMASTA 不宣稱它等同於客觀心理學真理。

---

## 8. 不自動排名

COMASTA 預設不回答：

    A 比 B 更像這個人。

它可以同時判定：

    A：SUPPORTED
    B：SUPPORTED
    C：PLAUSIBLE DEVIATION

因為不同的行為可能透過不同路徑成立。

---

## 9. 不自動修正

系統發現：

- 矛盾
- 偏離
- 資訊不足
- 支持薄弱

時，不應立刻替作者改寫人物。

它應該先把問題顯示出來。

作者保留最後的詮釋與創作權。

---

## 10. 未知仍然存在

即使系統已經建立完整的解釋路徑：

    已知人物條件
    ≠
    完整的人

COMASTA 可以描述目前能理解的部分。

但它不應宣稱已經描述完整的人。

---

## 核心評估原則

> 一套越成熟的系統，不應只是產生更確定的答案；它應該更精準地分辨：什麼可以理解、什麼目前沒有支持，以及什麼必須繼續保持未知。
