# MotorCare Online — PWA + Android

Web app: https://manartshop.github.io/motorcare-online-v5/
Android package: com.manartshop.motorcarev5

## Build
This repository uses GoogleChromeLabs Bubblewrap to package the existing PWA as a Trusted Web Activity. Bubblewrap can generate a signed Android App Bundle (AAB).

Google Play requires new apps and updates submitted from 31 August 2026 to target Android 16 / API 36 or higher.

## GitHub Actions secrets
Keep the signing key private and stable. Add these repository secrets before running the Android workflow:
- MOTORCARE_KEYSTORE_B64: base64-encoded Android keystore
- MOTORCARE_KEYSTORE_PASSWORD: keystore password
- MOTORCARE_KEY_PASSWORD: key password

The key alias expected by the workflow is android.

After a successful build, the AAB is available as the GitHub Actions artifact motorcare-online-aab. The workflow also generates .well-known/assetlinks.json from the signing certificate so the TWA can open in verified fullscreen mode.

Do not commit android.keystore or any password to the repository.