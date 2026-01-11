# Chargebacks cheatsheet

## Что это
Chargeback = клиент оспорил транзакцию через банк, деньги могут быть списаны обратно + штрафы.

## Основные драйверы
- Fraud (card not present)
- Customer dispute (не узнает мерчанта, недоволен сервисом)
- Processing errors (двойные списания, некорректный refund)
- Subscription/recurring issues

## Ops что делать
- Следить за chargeback rate по PSP/GEO/методу
- Требовать у PSP reason codes + evidence requirements
- Совместно с продуктом: descriptor, refund policy, support, anti-fraud rules
- Уметь объяснить "как снизить" (не обещая магию)
