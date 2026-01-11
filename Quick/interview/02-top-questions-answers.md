# Top questions (HR + hiring) — ответы по структуре

## 1) Что делаете, если упал approval rate?
- Scope: где/когда/насколько
- Сегментация: PSP/method/GEO/bank
- Проверки: top decline codes, timeouts, 3DS, изменения, логи
- Mitigation: fallback PSP / routing weights / disable method
- Коммуникация: внутренние + PSP (IDs, timestamps)
- Postmortem: root cause + prevention

## 2) Как вы работаете с PSP ежедневно?
- weekly scorecard, регулярные sync calls
- escalation paths, SLA по ответам
- контроль изменений/лимитов/правил
- совместные RCA и action items

## 3) Как объясняете сложные штуки не-тех людям?
- 1 слайд: симптом → влияние на деньги → план действий → ETA → риски
- без терминов, но с цифрами

## 4) Пример инцидента из опыта (STAR)
S: ...
T: ...
A: triage → mitigation → comms → fix
R: метрика восстановлена, добавили мониторинг/алерты

(вставь 2–3 истории в `03-story-bank-STAR.md`)
