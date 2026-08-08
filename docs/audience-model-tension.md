# Audience Model & Audience Tension — Content Architecture

**Дата:** 2026-08-07
**Статус:** Scaffolding — upstream-слой контент-пайплайна: Audience Model перед Tension Extraction
**Роль:** Определяет ICP для контента (не ICP продукта), audience tensions, и матрицу Product × Audience. Title — downstream компиляция, не генерация.

---

## Проблема: недостающий upstream-слой

До этого неявно предполагалось:

```
PRODUCT → TENSION → DRAMA → TITLE → READER
```

А должно быть:

```
PRODUCT
  ↓
AUDIENCE MODEL
  ↓
AUDIENCE TENSIONS
  ↓
EDITORIAL OPPORTUNITY
  ↓
DRAMA
  ↓
TITLE
  ↓
CONTENT
```

---

## 1. Драма не наша — драма зрителя

$0.75 vs $500 — это наш анализ материала. Но для зрителя это может быть вообще не драма.

**ICP для контента (Content ICP):** разработчик, который умеет делать SaaS, но работает по найму / фрилансит и хочет понять, какие продукты он может запускать самостоятельно.

Его напряжения:

- «Я умею кодить» VS «Я не знаю, что строить»
- «AI делает разработку дешёвой» VS «значит, теперь конкуренция должна быть ещё жестче»
- «Я могу вызвать любой API» VS «не понимаю, где здесь бизнес»
- «Я вижу тысячи AI tools» VS «не вижу, почему кто-то будет платить именно мне»
- «Хочу свой продукт» VS «не хочу превращаться в full-time founder»

$0.75 vs $500 — всего лишь evidence, которое мы можем использовать для одной из этих драм.

---

## 2. ICP для контента ≠ ICP продукта

| | Product ICP | Content ICP |
|---|---|---|
| **Кто** | Максим: Performance Marketer, $15k/mo traffic, creative bottleneck | Developer / software engineer |
| **Уже умеет** | — | coding ability, API knowledge, ability to ship |
| **Хочет** | campaign-ready creatives | autonomous income, products, leverage |
| **Struggles** | creative velocity | opportunity selection, buyer discovery, product judgment |
| **Beliefs** | — | «technical moat matters», «I need unique technology», «SaaS requires huge effort», «marketing/product is someone else's job» |
| **Behavior** | — | watches AI/startup/dev content, scrolls fast, suspicious of guru content, responds to concrete numbers |

Это другой объект моделирования. И он должен существовать **до** Tension Extraction.

---

## 3. Product Spec через две линзы

Не «Какие tensions есть в продукте?», а **«Какие факты продукта пересекаются с напряжениями ICP?»**

Матрица Product × Audience:

| Product fact | ICP tension | Potential content |
|---|---|---|
| Runway API | «AI capability ≠ product» | API → product |
| $0.75 | «AI должен уничтожить стоимость производства» | price shock |
| $500 studio | «если AI дешёвый, где value?» | value migration |
| no AI model | «нужна уникальная технология» | identity |
| workflow moat | «всё AI копируется за выходные» | defensibility |
| narrow buyer | «маленький niche = маленький business» | niche economics |
| batch-only | «больше features = лучше product» | deliberate constraints |
| $15k traffic | «creative is just production» | bottleneck |
| campaign-ready creative | «output = product» | value unit |

---

## 4. Audience-Conditioned Tension Extraction (Audience Lens)

Переименование pipeline: не Product → Tension Extraction, а **Product → Audience-Conditioned Tension Extraction**.

```
PRODUCT KNOWLEDGE
       │
       ▼
   AUDIENCE MODEL
       │
       ├── beliefs
       ├── desires
       ├── fears
       ├── misconceptions
       ├── ambitions
       └── unresolved tensions
       │
       ▼
PRODUCT × AUDIENCE INTERSECTION
       │
       ▼
TENSIONS WITH EVIDENCE
       │
       ▼
NARRATIVE OPPORTUNITIES
```

---

## 5. Drama — от ICP, не произвольно

Не «Какая драматизация лучше выглядит?», а **«Какую existing tension этого человека мы сейчас активируем?»**

Пример:

- ICP belief: «Чтобы сделать AI-продукт, надо иметь AI technology.»
- Product evidence: ACF использует готовый Runway API.
- Audience tension: I need unique technology VS valuable product can be built from commodity technology
- Editorial angle: Commodity → Product
- Title: «API есть у всех. Продукта — ни у кого.»

Title не «придуман». Он **скомпилирован** из tension ICP + evidence продукта.

---

## 6. Пять роликов — через пять разных tensions ICP

Не «5 лучших tensions продукта», а **5 разных tensions ICP**.

### T1 — Technology Anxiety
- ICP tension: «Мне нужна уникальная технология, иначе меня скопируют.»
- ACF evidence: SaaS without AI model
- Title: «Я построил SaaS без единой AI-модели»

### T2 — Opportunity Blindness
- ICP tension: «Я умею кодить, но не знаю, что строить.»
- ACF evidence: existing Runway capability → buyer → workflow
- Title: «Я нашёл бизнес в API, которым пользуются все»

### T3 — Commodity Anxiety
- ICP tension: «Если API доступен всем, продукта не существует.»
- ACF evidence: API ≠ workflow
- Title: «API есть у всех. Продукта — ни у кого.»

### T4 — Economics
- ICP tension: «AI снижает стоимость разработки, но где деньги?»
- ACF evidence: $0.75 → $500
- Title: «Я продаю за $500 то, что AI делает за $0.75»

### T5 — Scope Anxiety
- ICP tension: «Чтобы сделать серьёзный продукт, нужно строить огромную систему.»
- ACF evidence: 5–10 sec / batch-only / no realtime
- Title: «Я специально выкинул половину функций из AI-продукта»

Пять роликов имеют **разные причины существования** — разные ICP-tensions, разные evidence, разные drama.

---

## 7. Audience Tension — объект

```yaml
audience_tension:
  id: developer_001

  audience:
    role: software_developer

  current_belief:
    "valuable products require unique technology"

  desired_state:
    "I can create value around existing capabilities"

  tension:
    pole_a: commodity AI capability
    pole_b: differentiated product

  emotional_charge:
    curiosity: high
    skepticism: high
    identity_relevance: very_high

  content_evidence:
    - Runway API
    - ACF workflow
    - value_unit
    - moat

  eligible_drama:
    - contradiction
    - reversal
    - identity

  forbidden_drama:
    - generic AI hype
    - founder flex
```

`forbidden_drama` защищает от ситуации: «нашли очень кликабельную формулировку, которая привлекает вообще не тех людей».

---

## 8. Title — техническая компиляция

Pipeline:

```
CONTENT ICP
     ↓
AUDIENCE MODEL
     ↓
AUDIENCE TENSION
     ↓
PRODUCT EVIDENCE
     ↓
NARRATIVE OPPORTUNITY
     ↓
DRAMA MODE
     ↓
TITLE
```

Title generator получает **не Product Spec**. Он получает уже:

```
audience: ...
audience_tension: ...
evidence: ...
claim: ...
drama: ...
keywords: ...
```

И его задача: **сжать** существующую editorial opportunity в discoverable/clickable title, не меняя underlying claim. Это граница ответственности: title generator не придумывает смысл — только пакует.

---

## 9. Архитектурный вывод

Мы не производим драмы. Мы **обнаруживаем unresolved tensions у аудитории и используем продукт как evidence для их разрешения.**

Редакционная модель:

```
AUDIENCE
  │
  │ unresolved tension
  ▼
EDITORIAL QUESTION
  │
  │ needs evidence
  ▼
PRODUCT / RESEARCH
  │
  │ provides evidence
  ▼
NARRATIVE
  │
  │ packaged for attention
  ▼
TITLE
```

Отношение к Behavioral Design:

- **Audience model** определяет, какую tension вообще стоит активировать
- **Tension discovery** находит, каким фактом её можно сделать реальной
- **Drama selection** определяет, как предъявить её этому человеку
- **Behavioral operators** определяют, как провести его через материал
- **Title** — просто внешний индекс всего этого

Title действительно оказывается самым downstream и самым тупым элементом системы. Это правильное место для него.
