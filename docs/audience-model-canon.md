# Audience Model Canon

**Дата:** 2026-08-07
**Статус:** Reference — канон моделирования аудитории для контент-пайплайна
**Роль:** Upstream-слой: формализует Content ICP, Audience Tensions, и матрицу Product×Audience. На его основе генерируются Narrative Opportunities.

---

## Принцип

Content ICP ≠ Product ICP. Контент-аудитория — это не покупатель продукта. Это человек, чьи unresolved tensions продукт может разрешить через evidence.

Модель аудитории строится до Tension Extraction. Без неё нет Editorial Question — есть только «какие факты интересны».

---

## Структура Audience Model

```yaml
audience_model:
  # ── Кто ──
  role:              # профессиональная роль (developer, marketer, founder…)
  context:           # контекст: найм / фриланс / пет-проекты / без работы
  skill_level:       # что уже умеет делать руками
  technical_depth:   # насколько технически грамотен (low / medium / high)

  # ── Чего хочет ──
  desires:           # explicit wants (autonomous income, leverage, products…)
  ambitions:         # долгосрочные амбиции (стать founder, уйти из найма…)

  # ── Где застревает ──
  unresolved_tensions:  # внутренние конфликты — основа для hooks
    - pole_a:         # одно убеждение
      pole_b:         # противоречащее ему
      charge:         # emotional weight (curiosity/skepticism/anxiety/ambition)

  struggles:         # что не получается, несмотря на желание

  # ── Во что верит ──
  beliefs:           # убеждения о том, как устроен мир продуктов/технологий
  misconceptions:    # beliefs, которые продукт опровергает (evidence)

  # ── Как потребляет контент ──
  content_behavior:
    platforms:       # где смотрит (YouTube, Twitter, Reddit…)
    scroll_speed:    # fast / medium / slow
    trust_filters:   # чему доверяет (concrete numbers, code, data)
    distrust:        # чему не доверяет (guru content, generic advice, AI hype)

  # ── Триггеры ──
  stops_scrolling_for:   # какой контент останавливает (shock numbers, identity hooks…)
  clicks_away_from:      # какой контент отталкивает
```

---

## Worked Example: Developer ICP

```yaml
audience_model:
  role:              software_developer
  context:           employed_or_freelance — хочет пет-проекты, не хочет full-time founder
  skill_level:       production_capable (может собрать работающий продукт)
  technical_depth:   high (понимает API, архитектуру, деплой)

  desires:
    - autonomous income (не зависеть от работодателя)
    - product leverage (доход, масштабирующийся без линейного роста усилий)

  ambitions:
    - стать software artisan — создавать ценные продукты без найма
    - pet-project → платящие пользователи

  unresolved_tensions:
    - pole_a: "Я умею кодить"
      pole_b: "Я не знаю, что строить"
      charge: high_anxiety
    - pole_a: "AI делает разработку дешёвой"
      pole_b: "значит, конкуренция должна быть ещё жестче"
      charge: moderate_skepticism
    - pole_a: "Я могу вызвать любой API"
      pole_b: "не понимаю, где здесь бизнес"
      charge: high_curiosity
    - pole_a: "Вижу тысячи AI tools"
      pole_b: "не вижу, почему кто-то будет платить именно мне"
      charge: high_identity_relevance
    - pole_a: "Хочу свой продукт"
      pole_b: "не хочу превращаться в full-time founder"
      charge: moderate_ambition

  struggles:
    - opportunity selection (какой продукт строить из бесконечных возможностей)
    - buyer discovery (кто заплатит, если я сделаю Х)
    - product judgment (отличать ценный продукт от просто работающего)

  beliefs:
    - "technical moat matters" (защита — в уникальной технологии)
    - "I need a unique technology to build a unique product"
    - "SaaS requires huge effort (many features, complex architecture)"
    - "marketing/product is someone else's job (I'm a builder)"

  misconceptions:
    - "AI products require building AI models"
    - "more features = better product"
    - "narrow buyer = small market"
    - "commodity API = no defensibility"

  content_behavior:
    platforms: [YouTube, Twitter, Reddit]
    scroll_speed: fast
    trust_filters: [concrete_numbers, code, data, specific_products]
    distrust: [guru_content, generic_advice, AI_hype, founder_flex]

  stops_scrolling_for:
    - shock_numbers (price, speed, scale)
    - identity_hooks ("I built X without Y")
    - contrarian_claims with evidence
  clicks_away_from:
    - "10 ways to..."
    - inspirational quotes
    - no numbers, no evidence
```

---

## Метод: от Audience Model к Narrative Opportunity

```
AUDIENCE MODEL
       │
       ▼
AUDIENCE TENSIONS (unresolved)
       │
       ▼
PRODUCT EVIDENCE (какие факты продукта пересекаются с tensions)
       │
       ▼
EDITORIAL QUESTION (какую tension активируем этим роликом?)
       │
       ▼
DRAMA MODE (как предъявить tension этому человеку)
       │
       ▼
NARRATIVE OPPORTUNITY (tension + evidence + claim + drama → title candidates)
```

**Правило:** Title — последняя операция. Title generator получает уже готовый Narrative Opportunity и только пакует его в discoverable/clickable форму. Title generator не имеет права придумывать смысл.

---

## Матрица Product × Audience (Ad Creative Factory × Developer)

| Product fact | ICP tension | Narrative opportunity |
|---|---|---|
| SaaS without AI model | Technology Anxiety | «Я построил SaaS без единой AI-модели» |
| Runway API → buyer → workflow | Opportunity Blindness | «Я нашёл бизнес в API, которым пользуются все» |
| API ≠ workflow | Commodity Anxiety | «API есть у всех. Продукта — ни у кого.» |
| $0.75 → $500 | Economics | «Я продаю за $500 то, что AI делает за $0.75» |
| 5-10s, batch-only, no realtime | Scope Anxiety | «Я специально выкинул половину функций из AI-продукта» |

Пять роликов — пять разных ICP tensions, активированных разными evidence из одного продукта.

---

## Forbidden Drama

Каждый audience_tension имеет поле `forbidden_drama` — драмы, которые *нельзя* использовать с этой tension, потому что они привлекают не ту аудиторию или ломают Trust.

| Forbidden Drama | Почему |
|---|---|
| generic AI hype | Developer distrust: «guru content» — Trust ↓, clicks away |
| founder flex | Активирует не ту identity («я не founder») — Identity threat, не Identity hook |
| get-rich-quick framing | Привлекает arbitrage-аудиторию вместо product builders |
| fake exclusivity («секрет, о котором молчат»)| Trust ↓ (developer distrust: generic advice) |
