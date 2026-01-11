# Decline reason matrix (шаблон)

| Symptom/Code | Layer | Typical cause | Where to check | Action |
|---|---|---|---|---|
| Timeout | PSP/Gateway | provider latency/outage | gateway logs, PSP status | fallback PSP, increase timeout, escalate |
| Do not honor | Issuer | bank rejects w/o details | PSP response codes | сегментация GEO/bank, 3DS policy, alternative method |
| Invalid signature | Merchant | wrong signing / keys | gateway request logs | fix integration keys/signing |
| 3DS challenge fail | 3DS | user friction/timeout | 3DS metrics, device data | adjust 3DS rules, UX tips |
| Duplicate | Merchant/Gateway | retries w/o idempotency | idempotency logs | enforce idempotency, dedupe |
