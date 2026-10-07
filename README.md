# MooPuu.github.io

Root site for **https://moopuu.github.io/** — required to host the Android
**Digital Asset Links** statement at the origin root so the *Prompt Engineer*
Android app can verify itself and run as a fullscreen Trusted Web Activity
(no browser address bar).

## Files

| File | Purpose |
|---|---|
| `.well-known/assetlinks.json` | Lets `com.mahdikareem.promptengineer` handle all URLs on this origin |
| `index.html` | Small landing page with links to the app, mobile UI, APK and repository |
| `.nojekyll` | Disables Jekyll so the dot-directory `.well-known` is published as-is |

## 🔗 Links

- **Web app:** https://moopuu.github.io/prompt-engineer/
- **Mobile UI:** https://moopuu.github.io/prompt-engineer/mobile/
- **Android APK:** https://github.com/MooPuu/prompt-engineer/releases/tag/v1.5.0
- **Repository:** https://github.com/MooPuu/prompt-engineer

## Update the signing fingerprint

Regenerate the statement after rotating the APK signing key:

```powershell
apksigner verify --print-certs Prompt-Engineer-v1.5.0.apk
```

Paste the `SHA-256 digest` into `sha256_cert_fingerprints` as colon-separated uppercase hex.

**MIT License** · © 2026 **Mahdi Kareem**
