# MotorCare Online V5 / Bengkel Buyung

Mobile-first Customer + Mechanic frontend connected to Supabase project ojjifayhxbtcmztljaej.

## PWA
- Web App Manifest with 192px/512px PNG icons
- Service Worker
- Standalone display mode
- HTTPS deployment through GitHub Pages
- Android-friendly viewport and GPS permissions

GitHub Pages URL:
https://manartshop.github.io/motorcare-online-v5/

## Android / Google Play
Android packaging is intended to use Trusted Web Activity (TWA) with Bubblewrap.

Package ID:
com.manartshop.motorcarev5

From 31 August 2026, Google Play requires new apps and updates to target Android 16 / API 36 or higher.

A signed AAB must be produced with a protected upload keystore. Do not commit the keystore or its password to GitHub.

## Flow
Customer: sign in → choose service → GPS → create order → dispatch.
Mechanic: sign in → online → GPS → receive offer → accept/reject → update status.
