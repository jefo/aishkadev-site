# Production Brief — T1 «Ad Creative Factory»

**Дата:** 2026-08-07
**Тип:** Downstream production brief — передаётся тому, кто скрафтит ролик.
**Роль:** Все решения приняты upstream. Здесь — spoken script + визуальные спецификации. Тайминги — за скобками (director).

---

## Title

«Я сделал продукт для performance marketer'а за $149/мес. Вот почему он будет платить.»

## Кого цепляем (ICP)

Разработчик, employed/freelance, умеет кодить, не знает что строить.

**Активируемая tension:** coding ability VS no ideas.

**Что обещаем показать:** как из чужой AI-capability обнаруживается конкретный buyer с recurring economic value.

**Drama:** Discovery.

---

## Beat 1 — Promise

**Spoken:**
«Я сделал продукт для performance marketer'а за $149 в месяц. Почему он будет платить?»

**Visual:** Customer Profile
```
┌──────────────────────────────────┐
│ PERFORMANCE MARKETER             │
│                                  │
│ Budget       $15k / month        │
│ Goal         acquire customers   │
│ Bottleneck   creative throughput │
│                                  │
│                    $149 / month  │
└──────────────────────────────────┘
```

---

## Beat 2 — Anomaly

**Spoken:**
«Он вливает $15,000 в рекламу каждый месяц. Кампаний — десятки. А креативов дизайнер делает всего пять в неделю. Машина трафика есть — производство креативов за ней не успевает.»

**Visual:** Process Map
```
TRAFFIC ($15k)
    ↓
CAMPAIGNS (десятки)
    ↓
DESIGNER
    ↓
5 creatives / week
    ⚠️ BOTTLENECK
```
Третья величина (десятки кампаний) делает bottleneck очевидным: acquisition machine VS production throughput, который не поспевает.

---

## Beat 3 — Evidence

**Spoken:**
«Runway уже делает само видео за 75 центов. Значит, проблема вообще не в генерации.»

**Visual:** Capability Map
```
┌─────────────────────┐     ┌──────────────────────┐
│ AI CAPABILITY        │     │ CAMPAIGN NEED         │
│                      │     │                       │
│ Text → Video        │     │ Many launch-ready     │
│ $0.75               │     │ creatives             │
│ seconds             │     │                       │
└─────────────────────┘     └──────────────────────┘
           │                          │
           └──────── GAP ─────────────┘
```
Проблема не в генерации — проблема в gap между capability и need.

---

## Beat 4 — Discovery

**Visual first:**
Brief → 1 generation → **?** (тупик)

*Пауза.*

**Visual then:**
Brief → 10 variants → packaging → launch

**Spoken (после визуального inference):**
«Вот что ему на самом деле нужно. Не видео. Готовые к запуску варианты.»

**Грамматика (за кадром, для понимания структуры):** Opportunity Solution Tree
```
        BUYER OUTCOME
     MORE CREATIVE THROUGHPUT
               │
     ┌─────────┴─────────┐
     │                   │
Generate video     Produce campaigns
     │                   │
 Runway API        Creative Factory
                         │
               ┌─────────┼─────────┐
               │         │         │
             Brief    Variants   Export
```

**Ключевое:** зритель видит inference визуально до того, как слышит spoken. earn_the_insight происходит.

---

## Beat 5 — Value Unit

**Spoken:**
«Я продаю ему не генерацию видео. Я продаю launch-ready creative: бриф → варианты → упаковка → готово к запуску.»

**Visual:** Value Proposition Canvas
```
CUSTOMER JOB: Produce campaign creatives
    ↓
PAIN: Designer can't scale
    ↓
GAIN: Many launch-ready variants

        ↓ product delivers ↓

Brief → Generate → Variants → Export → Launch-ready
```

**Смена кадра:** RUNWAY video file → ACF campaign-ready creative.

---

## Beat 6 — Economic Resolution

**Spoken:**
«Студия: $300-500 за один креатив. Дни ожидания. Здесь: $149 в месяц за десятки креативов за минуты. Продукт меняет не цену. Он меняет саму единицу покупки.»

**Visual:** Before/After Unit Economics
```
OLD MODEL                  NEW MODEL
─────────────             ─────────────
Studio                     ACF

$300–500                   $149 / month
    │                           │
    ▼                           ▼
1 creative                 campaign batch
    │                           │
    ▼                           ▼
days                       minutes
```

**Value unit shift:**
```
OLD UNIT              NEW UNIT
─────────            ─────────
per creative          per workflow/month
$300–500              $149
```

---

## Beat 7 — CTA

**Spoken:**
«В следующем ролике — ещё один продукт, который можно построить поверх чужого API. Подпишись.»

**Visual:** System Diagram
```
Capability → Buyer → Product
```
Focus на Buyer. Сериализация — открывает следующий loop.

---

## Production notes

- **Тайминги:** не указаны — director решает.
- **Motion:** за скобками. Примитивы и переходы — из visual-narrative-lib (17 компонентов Svelte + brutalist тема).
- **Epistemic commitment:** $149 — design price (KNOWN). «Будет платить» — prediction (INFERRED). В ролике — willingness-to-pay hypothesis, не validated fact.
- **Не изобретать visuals:** все 6 визуальных дисциплин — канонические (semantic-native-representation mapping). Никаких ad hoc representations.
- **Trust firewall:** все цифры — из Product Spec. Ничего не додумано.
