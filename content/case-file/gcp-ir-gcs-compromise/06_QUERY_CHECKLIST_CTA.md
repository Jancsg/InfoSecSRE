# CTA ASSET — CHECKLIST DE QUERIES (para EP05 / comentarios)

Úsalo cuando comenten `GCP`. Puedes pegarlo en comentario partido o Notion/GitHub.

## Hypotheses to validate
1. SA storage actuando fuera de baseline
2. Origen IP no trusted
3. Tooling CLI (`gsutil`/`gcloud`) inesperado en workload identity
4. Privilege probing (`EnableService` denied)
5. Object read on high-value bucket

## Fields to pull (Cloud Audit Logs)
- `authenticationInfo.principalEmail`
- `callerIp`
- `callerSuppliedUserAgent`
- `methodName` / `method`
- `severity` / severity / status
- `resource` / `bucket_name` / object name
- timestamp (build sequence)

## Sequence pattern (alert logic mindset)
```
denied EnableService
→ bucket enumeration
→ storage.objects.get on sensitive object
→ same principalEmail
→ same callerIp / odd UA
```

## Detection ideas (defensive)
- SA + `storage.objects.get` + IP not in allowlist
- `ServiceUsage.EnableService` denied on non-admin SA
- `gsutil` UA on service accounts that should be API-only
- First-time access to `importantbucket`-class resources

## Analyst mistakes to avoid
- Only reviewing successful calls
- Starting at the object, not identity
- Treating every `objects.get` as benign read
- Ignoring failed privilege probes
