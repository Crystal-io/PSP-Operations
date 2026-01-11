# Metric drop triage — 15 вопросов

1) Что именно упало: approval, conversion, payout success, latency?
2) С какого времени (точка начала)?
3) Один PSP или несколько?
4) Один метод оплаты или все?
5) Один GEO/валюта/банк или широкая проблема?
6) Есть ли релизы/изменения последние 24–48ч?
7) Что в логах gateway: 4xx/5xx, timeouts, signature?
8) Что говорит PSP: incident? изменения правил? лимитов?
9) Какие топ decline codes выросли?
10) Есть ли рост 3DS challenge/timeout?
11) Изменились ли antifraud/AML правила?
12) Есть ли рост дубликатов / retries?
13) Webhooks приходят? не задваиваются?
14) Это проблема upstream (issuer/acquirer) или integration?
15) Что можно быстро сделать как mitigation? (fallback PSP, отключить метод, увеличить timeout, rollback routing rule)
