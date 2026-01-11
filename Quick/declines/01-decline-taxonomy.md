# Declines taxonomy (быстро)

## Уровни причин
1) Merchant / Integration
- invalid signature, bad request, amount/currency mismatch, duplicate
2) PSP layer
- provider rules, limits, risk policies, routing misconfig, outage
3) Acquirer / Issuer
- do not honor, insufficient funds, card restrictions, geo restrictions
4) 3DS/SCA
- friction, challenge failed, timeout, device/browser issues
5) Fraud/AML
- velocity checks, blacklists, suspicious patterns

## Soft vs Hard
- Soft: можно повторить/перезапустить (timeouts, do not honor, network issues)
- Hard: требует изменения параметров/метода (invalid card, stolen, permanent restrictions)
