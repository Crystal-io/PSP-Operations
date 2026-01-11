# Incident triage checklist (коротко)

- [ ] Зафиксировать время начала
- [ ] Определить scope: PSP / method / GEO
- [ ] Снять 3 метрики: approval, timeouts/latency, top decline codes
- [ ] Проверить последние изменения (routing/risk/release)
- [ ] Проверить webhooks delivery + duplicates
- [ ] Принять mitigation: fallback / disable / rollback
- [ ] Оповестить внутренние команды (следующее обновление через 30 мин)
- [ ] Написать PSP с примерами (IDs + timestamps)
- [ ] После стабилизации — короткий postmortem
