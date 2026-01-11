# Provider comms templates

## A) Инцидент / деградация
Тема: [SEV-?] Payment degradation — {PSP} — {method} — started {time UTC}

Привет!
Наблюдаем деградацию:
- Start: {timestamp}
- Impact: approval {x}% → {y}%, timeouts +{n}%
- GEO/method: {geo}, {method}
- Samples: {correlation IDs / order IDs}

Подскажите, есть ли инцидент или изменения на вашей стороне? 
Нужны: текущий статус, ETA, рекомендации, и лог/trace по указанным ID.

## B) Запрос по declines
Тема: Increase in issuer declines — request for breakdown

Привет!
Выросли declines по коду {code} с {x}% до {y}% начиная с {time}.
Можно ли дать breakdown по банкам/issuer и возможные причины? 
Есть ли рекомендации по 3DS/risk настройкам?
