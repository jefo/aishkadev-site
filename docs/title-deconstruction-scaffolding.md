# Title Deconstruction — «Я сделал продукт для performance marketer'а. Он БУДЕТ платить $149/мес. Вот почему.»

**Дата:** 2026-08-07
**Статус:** Scaffolding — разбор одного title как архитектурного образца
**Роль:** Показать, как работает title: не генерация, а компиляция из ICP × tension × evidence × promise. Разбор epistemic commitment: KNOWN / INFERRED / VALIDATED.

---

## 1. Что здесь реально работает (архитектурно, не стилистически)

### Buyer specificity

«performance marketer» — сразу отсекает абстрактное «Я создал AI SaaS» и говорит: я нашёл конкретного человека с конкретной экономикой. Для developer ICP это очень хороший signal, потому что проблема «как найти того, кто заплатит» является частью их unresolved tension.

### $149/month сильнее, чем $149

Потому что это не цена. Это **economic relationship**:

```
buyer
  ↓
recurring problem
  ↓
recurring value
  ↓
recurring payment
```

Title обещает показать не просто «продукт стоит $149», а **почему buyer будет продолжать платить**. Это уже product thinking.

### «Вот почему» создаёт open loop

Неизвестно, что именно является причиной willingness-to-pay: экономия? workflow? volume? замена агентства? ROI? switching cost? convenience? Здесь можно использовать `delay resolution` (BD operator).

---

## 2. Проблема epistemic commitment

Слово «БУДЕТ» создаёт очень сильное epistemic commitment. Если нет реального buyer validation, это может ударить по Trust (BD-переменная).

У нас есть: Product Spec → Growth tier = $149/mo. Но это доказывает: **цена продукта = $149**, а не: **Max will pay $149 every month**. Это разные claims.

**Три уровня epistemic commitment:**

| Уровень | Claim | Evidence | Title |
|---|---|---|---|
| **KNOWN** | $149 is the designed price | Product Spec | — |
| **INFERRED** | buyer has sufficient economic value to rationally pay $149 | Product Spec + JTBD + economics | «Почему performance marketer будет платить мне $149 каждый месяц» |
| **VALIDATED** | actual buyer pays $149 repeatedly | реальный платёж | «Я сделал продукт, за который performance marketer платит $149/мес. Вот почему.» |

**Правило:** каждый компонент Title Promise должен быть evidence-backed. Если claim — INFERRED, title должен это отражать (вопросительная форма, «будет»→«почему будет»). Если VALIDATED — утвердительная форма допустима.

---

## 3. Title Grammar

```
TITLE PROMISE = [WHO] + [ECONOMIC COMMITMENT] + [RECURRENCE / SCALE] + [OPEN LOOP]
```

| Компонент | В данном title | Роль |
|---|---|---|
| WHO | performance marketer | Конкретный buyer — отсекает абстракцию |
| ECONOMIC COMMITMENT | $149 | Сумма — создаёт economic expectation |
| RECURRENCE | каждый месяц | Подписка, не разовая — economic relationship |
| OPEN LOOP | Вот почему | Что создаёт willingness-to-pay? → delay resolution |

**Варианты в зависимости от epistemic commitment:**

- INFERRED: «Почему performance marketer будет платить мне $149 каждый месяц» — вопрос, не утверждение
- VALIDATED: «Я сделал продукт, за который performance marketer платит $149/мес. Вот почему.» — утверждение
- Design price (KNOWN, не inferred): «Я сделал продукт для performance marketer'а за $149/мес. Вот почему он будет платить.» — design price как факт, платёж как prediction

---

## 4. Content Promise — counterpart Product Intent

В продукте: «Почему этот buyer будет платить за эту конфигурацию продукта?» (Product Intent)

В контенте: «Почему этот viewer должен захотеть посмотреть этот ролик?» (Content Promise)

Для каждого ролика:

```yaml
content_promise:
  audience: developer
  unresolved_tension:
    "I can build, but I don't know what people will pay for"

  evidence:
    buyer: performance marketer
    price: $149/month
    economic_value: ...

  promise:
    "I'll show why this buyer would pay $149/month"

  open_loop:
    "What creates the willingness to pay?"
```

Title генерируется не из продукта. Он генерируется из: **ICP × unresolved tension × evidence × promise.**

---

## 5. Правила

1. **Title generator не придумывает смысл** — пакует Content Promise в discoverable/clickable форму
2. **Каждый компонент Promise evidence-backed** — epistemic commitment соответствует уровню validation
3. **Open loop должен быть реальным** — «вот почему» только если есть неочевидная причина willingness-to-pay
4. **Aggression ∈ Trust** — чем агрессивнее title, тем выше Trust-риск. Цифры и buyer specificity снижают этот риск (конкретика вместо хайпа)
