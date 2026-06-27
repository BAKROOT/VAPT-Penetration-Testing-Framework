# Mobile Application Testing Checklist

Aligned with OWASP MASVS and the Mobile Application Security Testing Guide (MASTG). Covers iOS and Android. Mark each item Pass / Fail / N/A / Review and log failures as findings.

## Architecture & Setup
- [ ] Obtain build/IPA/APK and identify platform and frameworks
- [ ] Set up instrumented test device/emulator
- [ ] Identify backend APIs and third-party SDKs

## Data Storage
- [ ] Check for sensitive data in local storage (DBs, plists, shared prefs)
- [ ] Check for sensitive data in logs
- [ ] Verify keychain/keystore usage for secrets
- [ ] Check for sensitive data in app backups
- [ ] Verify no sensitive data in screenshots/cache

## Cryptography
- [ ] Verify strong, current cryptographic algorithms
- [ ] Check for hard-coded keys/secrets in the binary
- [ ] Verify secure random number generation

## Authentication & Session
- [ ] Test authentication and session handling
- [ ] Test biometric/local authentication bypass
- [ ] Verify token storage and invalidation

## Network Communication
- [ ] Verify TLS used for all traffic
- [ ] Test certificate pinning (and bypass resistance)
- [ ] Check for cleartext traffic

## Platform Interaction
- [ ] Review requested permissions for least privilege
- [ ] Test exported components (Android: activities, services, providers)
- [ ] Test deep link / URL scheme handling
- [ ] Test WebView configuration (JS bridges, file access)

## Code Quality & Resilience
- [ ] Check for debug flags / verbose logging in release builds
- [ ] Assess anti-tampering / root/jailbreak detection (if required)
- [ ] Review obfuscation (where applicable)

## Backend / API
- [ ] Apply the API security checklist to the app's backend
