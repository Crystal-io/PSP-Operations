# Deposit flow (L2) + точки контроля

## Типовой flow
1) Клиент выбирает метод оплаты в cashier
2) Система формирует payment intent / order
3) Routing выбирает PSP (или каскад)
4) Redirect / SDK / APM flow (зависит от метода)
5) PSP → acquirer → issuer (авторизация)
6) 3DS/SCA (если требуется)
7) Ответ (sync) + webhook/callback (async подтверждение)
8) Запись в ledger / баланс / отображение статуса в кабинете

## Где чаще всего ломается (и что смотреть)
- До PSP: ошибки в request, signature, amount/currency, merchant config → логи gateway, request/response
- На PSP: timeouts, provider outage, PSP rules → provider status page + correlation IDs
- Acquirer/issuer: declines codes → decline reason mapping + geo/bank patterns
- 3DS: friction, timeout, challenge fail → 3DS step metrics + device/browser issues
- Webhooks: не дошли/дубли → webhook logs, idempotency keys, retry policy

## What to ask internally
- Что менялось последние 24–48ч (routing, risk rules, 3DS настройки, UI кассы)?
- Один PSP или несколько? Один GEO или все?
- Это step-level drop или общий?
