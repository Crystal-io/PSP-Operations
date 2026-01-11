# Payout flow (L2) + точки контроля

## Типовой flow
1) Клиент инициирует вывод (cashier)
2) Pre-checks: KYC, AML, лимиты, баланс, risk flags
3) Создается payout request → routing выбирает провайдера
4) Отправка в PSP/провайдера
5) Асинхронные статусы: pending → processing → completed / failed / reversed
6) Ledger update + уведомление клиента

## Где ломается
- KYC/AML gate: "stuck" из-за compliance → причины hold + SLA на ручные проверки
- Provider latency/outage → timeout rate, provider incident
- Bank details/format → validation errors
- Status mismatch: provider says success, у нас pending → reconciliation checks, webhook delivery

## Что важно в Ops
- SLA по выплатам (time-to-complete)
- процент stuck payouts
- причины отказов/отмен
