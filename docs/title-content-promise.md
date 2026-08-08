# Title Content Promise — Formal Reference

**Дата:** 2026-08-07
**Статус:** Reference — формальный канон генерации title из Content Promise
**Роль:** Title = downstream компиляция из ICP × unresolved tension × evidence × promise. Title generator не придумывает смысл — пакует Content Promise в discoverable/clickable форму.

---

## Title Grammar

```
TITLE PROMISE = [WHO] + [ECONOMIC COMMITMENT] + [RECURRENCE / SCALE] + [OPEN LOOP]
```

| Компонент | Определение | Пример |
|---|---|---|
| **WHO** | Конкретный buyer — отсекает абстракцию | performance marketer |
| **ECONOMIC COMMITMENT** | Сумма или эквивалент — создаёт economic expectation | $149 |
| **RECURRENCE / SCALE** | Подписка, объём, частота — economic relationship | каждый месяц |
| **OPEN LOOP** | Что создаёт willingness-to-pay? | Вот почему |

---

## Epistemic Commitment: три уровня

Каждый компонент Promise должен быть evidence-backed. Уровень validation определяет форму title.

| Уровень | Claim | Evidence | Форма title |
|---|---|---|---|
| **KNOWN** | $149 is the designed price | Product Spec | Утверждение: «за $149/мес» |
| **INFERRED** | buyer has sufficient economic value to pay $149 | Spec + JTBD + economics | Вопрос: «почему будет платить $149» |
| **VALIDATED** | actual buyer pays $149 repeatedly | реальный платёж | Утверждение: «платит $149/мес» |

**Правило:** claim не должен превышать epistemic commitment. INFERRED → вопросительная форма или prediction («будет»). VALIDATED → утвердительная форма («платит»).

---

## Content Promise — аналог Product Intent для контента

В продукте: «Почему этот buyer будет платить за эту конфигурацию продукта?» (Product Intent)

В контенте: «Почему этот viewer должен захотеть посмотреть этот ролик?» (Content Promise)

```yaml
content_promise:
  audience:                 # Content ICP
    role: developer
  unresolved_tension:      # какую ICP-tension активируем
    pole_a: "I can build"
    pole_b: "I don't know what people will pay for"
  evidence:                # из Product Spec
    buyer: performance marketer
    price: $149/month
    economics: $0.75 cost → up to $500 value
  promise:                 # что обещаем показать
    "why this buyer would pay $149/month"
  open_loop:               # что остаётся неизвестным
    "What creates the willingness to pay?"
  drama_mode:              # из каталога Drama Operators
    discovery               # «я нашёл» — для tensions про «что строить»
```

---

## Pipeline: от Content Promise к Title

```
CONTENT ICP
     ↓
UNRESOLVED TENSION
     ↓
PRODUCT EVIDENCE
     ↓
CONTENT PROMISE
     ↓
TITLE (downstream компиляция)
```

Title generator получает готовый Content Promise. Его задача: **сжать** editorial opportunity в discoverable/clickable title, не меняя underlying claim.

---

## Правила

| # | Правило |
|---|---|
| 1 | Title generator не придумывает смысл — только пакует Content Promise |
| 2 | Каждый компонент Promise evidence-backed — epistemic commitment ≤ уровень validation |
| 3 | Open loop должен быть реальным — «вот почему» только если есть неочевидная причина |
| 4 | Конкретика (buyer + цифры) снижает Trust-риск агрессивного hook |
| 5 | Абстрактные claims («создал SaaS», «убил индустрию») — запрещены. Только конкретный buyer + конкретная цифра. |
| 6 | Concrete over meta: не «как я нашёл идею», а «для кого я сделал и почему он платит» |

---

## Worked Example: Ad Creative Factory → Content Promise → Title

**ICP:** developer, employed/freelance, «I can build but I don't know what people will pay for»

**Content Promise:**
```yaml
audience:
  role: developer
unresolved_tension:
  pole_a: "I can build"
  pole_b: "I don't know what people will pay for"
evidence:
  buyer: performance marketer (Максим, $15k/mo traffic)
  pain: creative bottleneck — 5/week when 20-30 needed
  product: Ad Creative Factory — brief → generate → variants → export
  price: $149/month (Growth tier)
  economics: $0.75/creative cost, $300-500/creative studio price
promise:
  "why this buyer would pay $149/month"
open_loop:
  "What creates the willingness to pay? (Not AI quality — workflow and value unit)"
drama_mode:
  discovery
```

**Title (INFERRED, т.к. платёж не validated):**
«Почему performance marketer будет платить мне $149 каждый месяц»

**Title (VALIDATED, если платёж подтверждён):**
«Я сделал продукт, за который performance marketer платит $149/мес. Вот почему.»

**Title (KNOWN — design price, prediction):**
«Я сделал продукт для performance marketer'а за $149/мес. Вот почему он будет платить.»

---

## Forbidden Patterns

| ❌ | Почему | ✅ |
|---|---|---|
| «Я создал AI SaaS за выходные» | Абстрактно, нет buyer, нет экономики | «Я сделал продукт для performance marketer'а за $149/мес» |
| «Этот стартап убьёт рекламные агентства» | Hyperbole без evidence | «Студия берёт $500 за креатив. Я делаю за $0.75.» |
| «10 способов заработать на AI» | Список, не продукт. Meta-advice. | Конкретный продукт для конкретного buyer |
| «Как я нашёл идею на миллион» | Процесс, не результат. Meta. | «Вот почему он платит $149/мес» |
