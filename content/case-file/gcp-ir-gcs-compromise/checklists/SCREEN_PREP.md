# SCREEN PREP — LOG SCENES TO CAPTURE

Prepara estas “escenas” en tu visor de logs (LetsDefend lab / recreate) antes de grabar.

## Scene pack
1. **Identity close-up** — row with `authenticationInfo.principalEmail` = `cloud-storage-helper@cryptostartup.iam.gserviceaccount.com`
2. **Project context** — `cryptostartup` visible once (EP01 optional)
3. **IP close-up** — `callerIp` = `178.132.108.38`
4. **UA close-up** — `callerSuppliedUserAgent` showing Macintosh
5. **UA tool** — user agent containing `gsutil`
6. **Error filter view** — list filtered to errors/denied
7. **Fail method** — `...ServiceUsage.EnableService` clearly readable
8. **Bucket** — `importantbucket` / bucket_name field
9. **Exfil method** — `storage.objects.get` (methodName)
10. **Object** — `secretcode.java` in resource/object field

## Capture method
For each scene:
- Hold still 3s
- Move cursor to field
- Hold 2s
- Slight scroll only if needed for next field

## Naming files
```
SCR_EP01_principalEmail.mp4
SCR_EP02_callerIp.mp4
SCR_EP02_userAgent.mp4
SCR_EP03_EnableService_FAIL.mp4
SCR_EP04_bucket.mp4
SCR_EP04_objects_get.mp4
SCR_EP04_secretcode.mp4
SCR_EP04_gsutil.mp4
```
