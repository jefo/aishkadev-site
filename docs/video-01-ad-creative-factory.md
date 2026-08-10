# YouTube Video — 01: Ad Creative Factory: анатомия продукта

## Title

«Ad Creative Factory: анатомия продукта, за который платят $149/мес»

## Hook

«Это не SaaS для генерации видео. Это механизм смены economics performance-маркетинга.»

## Body

Материал: `webapp/src/content/products/ad-creative-factory.mdx` (Product Anatomy + Intent Resolution + Product Prism). Каждый блок прозы — beat, плотность сохранена.

| Beat | Move | Spoken | Visual |
|---|---|---|---|
| 1 | **expose** — ввести продукт | «Ad Creative Factory — не SaaS для генерации видео. Это механизм смены economics performance-маркетинга. Разберём, почему buyer, value unit, pricing и moat собраны именно так — и как это меняет экономику маркетолога, который льёт $15,000 в месяц на трафик.» | Service Flow (продукт как механизм) |
| 2 | **destabilize** — дизайн-спейс: кто buyer и какая работа | «Один buyer: Performance Marketer — Максим. Покупает трафик, тестирует креативы. Не Creative Pro, не Enterprise. Его JTBD трёхслойный: functional — 50 креативов в час; emotional — контроль над creative pipeline; social — масштабирование быстрее конкурентов. И это не "все, у кого есть API-ключ" — это один человек с одной работой.» | Customer Profile (Максим, JTBD 3 слоя) |
| 3 | **destabilize** — дизайн-спейс: value unit и pricing | «Value unit: креатив, готовый к запуску в рекламный кабинет. Не видеофайл, не API-вызов. Pricing: пакеты креативов — $49, $149, $499 в месяц. Не per-API-call. Юнит-экономика: $0.75 за креатив против $500 за креатив у студии. Вот это число — не маркетинг, это смена категории цены.» | Value Unit + Before/After Economics |
| 4 | **destabilize** — дизайн-спейс: режим, фрейминг, moat | «Production mode: batch — бриф, генерация, вариации, экспорт. Не интерактивный диалог. Competitive framing: против студийного способа решения, не против Pika и Kling. Moat — три слоя: workflow сильнее endpoint; buyer knowledge сильнее feature list; pricing model сильнее API pricing.» | Process Map + System Diagram |
| 5 | **destabilize** — доминантное напряжение | «Доминирующее напряжение: глубина moat против времени до рынка. Три слоя moat плюс четыре компонента плюс осознанные границы — это время на разработку. Каждый слой moat — структурная защита, но конкуренты с "генератором видео" выходят быстрее. Вот цена, которую платит такой дизайн.» | Tension Map (moat depth vs time to market) |
| 6 | **reframe** — интент: L1 + L2 | «Продуктовый интент: создать продукт для performance marketer'а, решающий трёхслойный JTBD через глубокую buyer knowledge, value proposition "замена агентства" и трёхслойный moat, при batch-only режиме, 5–10-секундном формате и осознанных границах. Семь решений: один buyer с трёхслойным JTBD — не все; value unit — креатив, готовый к запуску, не видеофайл; value proposition против студии — pain relievers плюс gain creators; четыре компонента — Creative Generator, Variation Engine, Brief Interface, Campaign Packager; исключены Realtime и Ad Platform Integration из v1; pricing — пакеты креативов, не per-API-call; moat — три слоя.» | Opportunity Solution Tree (4 компонента) |
| 7 | **system-expand** — интент: L3 последствия | «Что из этого следует. $0.75 за креатив против $500 у студии — это смена economics, не скидка. Трёхслойный JTBD: продукт покупают за контроль над кампанией, не за генерацию видео. Batch плюс компонентная архитектура дают предсказуемую cost structure. И главное: конкурент с тем же самым API не получает тот же продукт — потому что продукт это не вызовы API, а система решений.» | Before/After Economics |
| 8 | **false-intuition** — грань 1: Feature Frame → Service Frame | «Первая грань призмы. "SaaS для генерации креативов" — это рамка инструмента. Сдвиг: механизм предоставления услуги. Ценность не в инструменте, а в service flow креативов без ожидания студии. Ты покупаешь не софт — ты покупаешь поток результата.» | Service Flow |
| 9 | **false-intuition** — грань 2: Feature List → Value Unit | «Вторая грань. Максим покупает не генерацию видео, а креатив, готовый к запуску. Видеофайл — реализация. Креатив — продукт. Пока ты продаёшь "генерацию", ты в commodity. Как только продаёшь готовый к запуску креатив — ты в продукте.» | Value Unit (видеофайл vs креатив) |
| 10 | **false-intuition** — грань 3: Pricing Table → Economics Shift | «Третья грань. $149 в месяц — не цена продукта. Это цена смены economics: с $300–500 за креатив на $0.75. Таблица цен не конкурирует с таблицей цен студии — она конкурирует с самой структурой их бизнеса.» | Before/After Unit Economics |
| 11 | **identity-synthesize** — грань 4: API Competition → Activity System Moat | «Четвёртая грань. Moat — не Runway API. API доступен всем. Moat — система деятельности: workflow плюс buyer knowledge плюс pricing model. Конкурент может купить тот же API. Он не может купить решения, которые мы приняли о buyer'е и о форме продукта.» | Activity System Map |
| 12 | **identity-synthesize** — грань 5: Product → Platform | «Пятая грань. Ad Creative Factory — entry point. Capability Inventory один и тот же, меняется конфигурация под buyer. Один и тот же Runway API — фабрика креативов для маркетолога, видео-конвейер для e-commerce, генератор клипов для студии. Продукт — это выбор конфигурации под конкретную работу.» | Platform Map (одна capability → N конфигураций) |
| 13 | **extract** — что уносим | «Итог анатомии. Продукт собирается из решений: кто buyer, какая работа, какая единица ценности, против кого конкурируем, чем защищены. Каждое решение объяснено не технической возможностью, а работой buyer'а. И если ты видишь API и спрашиваешь "какую работу можно закрыть" — следующий ролик покажет, как именно читать любой API с продуктовой оптикой.» | System Diagram (Capability → Buyer → Product) |

## CTA

«Следующий ролик: от endpoint к продукту — восемь мысленных переходов на примере Runway. Подпишись, чтобы не пропустить.»

## Description

Разбор product shape Ad Creative Factory: почему buyer, value unit, pricing и moat собраны именно так — и как это меняет economics performance-маркетолога. Product Anatomy: дизайн-спейс (buyer, JTBD, value unit, pricing, production mode, framing, moat), доминантное напряжение, интент-резолюция (L1/L2/L3) и пять граней product prism: Feature Frame → Service Frame, Feature List → Value Unit, Pricing Table → Economics Shift, API Competition → Activity System Moat, Product → Platform.

Ключевые цифры: $0.75/креатив против $500 студия; пакеты $49/$149/$499; один buyer, трёхслойный JTBD; moat из трёх слоёв.

## Production notes

- **Trust firewall:** все цифры — из Product Spec и Product Anatomy (MDX). Ничего не додумано. $15,000 трафика — из buyer persona (Spec §1). $300–500/креатив — из Spec §5. $0.75 — Spec §5.
- **Epistemic commitment:** $149 — design price (KNOWN). «Меняет economics» — расчёт (INFERRED), формулируется как prediction. Платёж не validated — никаких «уже платит».
- **Плотность:** каждая единица информации MDX перенесена: Design Space (7 осей) — beats 2-4, Dominant Tension — beat 5, Intent Resolution (L1/L2/L3) — beats 6-7, Prism 5 граней — beats 8-12. Ничего не отброшено.
- **Visual:** все дисциплины канонические (semantic-native-representation): Customer Profile, Process Map, Opportunity Solution Tree, Value Unit, Before/After Economics, Activity System, Platform Map. Не ad hoc.
- **Тайминги:** за скобками — director.
