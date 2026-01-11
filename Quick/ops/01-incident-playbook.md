# Incident playbook (payments)

## 1) Detect
- Alert: approval down / timeouts up / provider errors up
- Confirm with dashboard + logs (scope)

## 2) Triage (15–30 min)
- Segment: PSP / method / GEO / time window
- Identify top errors/codes
- Decide severity (SEV1/2/3)

## 3) Mitigate (быстрые действия)
- Enable fallback PSP / change routing weight
- Disable failing method temporarily
- Adjust timeouts/retries (осторожно)
- Rollback last change if obvious correlation

## 4) Communicate
- Internal: status + ETA next update
- Provider: correlation IDs, timestamps, samples, impact metrics

## 5) Resolve + Postmortem
- Root cause
- Prevent recurrence (monitoring, alerts, playbooks, tests)
