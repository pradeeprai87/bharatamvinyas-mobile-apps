# Cloud Education ERP – Android app

School ERP mobile app (Flutter) for students, parents, teachers, drivers, principals and accountants.
This build talks to the **live server**:

- API base: `https://edu.bharatamvinyas.com/api/v1`
- Web app: https://edu.bharatamvinyas.com/login

## Current build

| | |
|---|---|
| File | `cloud-edu-erp-live-20261004.apk` |
| Package | `in.cloudedu.cloud_edu` |
| Version | `0.1.0` (versionCode 1) |
| Built | 2026-10-04 |
| Size | 67,169,772 bytes (about 64 MiB / 67 MB) |
| SHA256 | `39d19c08881181b592e6d260a9c0bb3896ea7bd0d8c3dc42d2f1984c356da91e` |
| Signing | debug key (test build, not a Play Store release) |
| ABIs | arm64-v8a, armeabi-v7a, x86_64 (fat APK) |
| Permissions | INTERNET, ACCESS_NETWORK_STATE, ACCESS_FINE/COARSE_LOCATION |

Download:

- Release (recommended): https://github.com/pradeeprai87/bharatamvinyas-mobile-apps/releases/tag/cloud-education-erp-v20261004
- Direct file: https://github.com/pradeeprai87/bharatamvinyas-mobile-apps/raw/main/cloud-education-erp/cloud-edu-erp-live-20261004.apk

## Install on Android

1. **Uninstall any older Cloud Edu / `cloud_edu` build first.** Earlier test builds pointed to a local backend (127.0.0.1 / LAN IP) and, if left installed, will keep failing to log in.
2. Open the download link on the phone and download the APK.
3. Open the file. When Android asks, allow **Install unknown apps** for your browser or file manager (Settings -> Apps -> Special access -> Install unknown apps).
4. Tap **Install**. If Play Protect warns about an unknown developer (debug-signed test build), choose **Install anyway**.
5. Open **cloud_edu**, enter email and password, sign in. The phone needs internet access.

Verify the download (optional): `sha256sum cloud-edu-erp-live-20261004.apk` must match `SHA256SUMS`.

## Login accounts

Passwords are **not** stored in this repository. The owner gives them separately.

| Account | Role | Notes |
|---|---|---|
| `ops@bharatamvinyas.com` | Platform super admin (SaaS) | Password from owner |
| `admin@bharatamvinyas.com` | Platform admin (SaaS) | Password from owner |
| `crm@bharatamvinyas.com` | SaaS CRM | Password from owner |
| `support@bharatamvinyas.com` | SaaS support | Password from owner |
| School users (owner, principal, teacher, accountant, parent, student, driver) | School roles | Created per school; sign in at https://edu.bharatamvinyas.com/login (same credentials in the app) |

## Known behaviour

- The SaaS roles (`ops@`, `admin@`, `crm@`, `support@`) can sign in in the app, but the mobile screens are designed for **school roles**, so those accounts see a limited or empty experience. Use the web panels for SaaS administration.
- Debug-signed build: it cannot be updated over a build signed with a different key; uninstall first if install fails with "package conflicts".

## Troubleshooting

- "Cannot connect" / login fails: uninstall older builds, make sure the phone is online, and open https://edu.bharatamvinyas.com/api/v1/health in the phone browser (should return OK).
- Install blocked: enable **Install unknown apps** for the app you opened the APK from.

Superseded location: an identical earlier copy exists at `pradeeprai87/bharatamvinyas.com` under `APKs/`; use this repository instead.
