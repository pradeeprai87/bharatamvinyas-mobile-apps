# Cloud Education ERP – Android app

School ERP mobile app (Flutter) for students, parents, teachers, drivers, principals and accountants.
This build talks to the **live server**:

- API base: `https://edu.bharatamvinyas.com/api/v1`
- Web app: https://edu.bharatamvinyas.com/login

## Current build

| | |
|---|---|
| File | `cloud-edu-erp-live-20261005.apk` |
| Package | `in.cloudedu.cloud_edu` |
| Version | `0.1.0` (versionCode 1) |
| Built | 2026-10-05 |
| Size | 65,190,702 bytes (about 62 MiB / 65 MB) |
| SHA256 | `e49e21192404ea419bc3f0772f633e66b5914edecc35523584fa9c5949787cba` |
| Signing | debug key (test build, not a Play Store release) |
| ABIs | arm64-v8a, armeabi-v7a, x86_64 (fat APK) |
| Permissions | INTERNET, ACCESS_NETWORK_STATE, ACCESS_FINE/COARSE_LOCATION |

Download:

- Release (recommended): https://github.com/pradeeprai87/bharatamvinyas-mobile-apps/releases/tag/cloud-education-erp-v20261005
- Direct file: https://github.com/pradeeprai87/bharatamvinyas-mobile-apps/raw/main/cloud-education-erp/cloud-edu-erp-live-20261005.apk

The 2026-10-04 release stays available at https://github.com/pradeeprai87/bharatamvinyas-mobile-apps/releases/tag/cloud-education-erp-v20261004.

## Install on Android

1. **Uninstall any older Cloud Edu / `cloud_edu` build first.** Earlier test builds pointed to a local backend (127.0.0.1 / LAN IP) and, if left installed, will keep failing to log in.
2. Open the download link on the phone and download the APK.
3. Open the file. When Android asks, allow **Install unknown apps** for your browser or file manager (Settings -> Apps -> Special access -> Install unknown apps).
4. Tap **Install**. If Play Protect warns about an unknown developer (debug-signed test build), choose **Install anyway**.
5. Open **cloud_edu**. Choose the organization (Bharatam Vinyas for platform staff, or the school), then enter email and password. The phone remembers the organization and email, not the password. The phone needs internet access.

Verify the download (optional): `sha256sum cloud-edu-erp-live-20261005.apk` must match `SHA256SUMS`.

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

- Platform staff and school staff use this same app. After a correct login the phone opens that role's home: schools, quotations, invoices, subscriptions and support for Bharatam Vinyas; the school desks for a school.
- The organization search on the sign-in screen needs the 2026-10-05 server code. Until that deploy, the list cannot load.
- Debug-signed build: it cannot be updated over a build signed with a different key; uninstall first if install fails with "package conflicts".

## Troubleshooting

- "Cannot connect" / login fails: uninstall older builds, make sure the phone is online, and open https://edu.bharatamvinyas.com/api/v1/health in the phone browser (should return OK).
- Install blocked: enable **Install unknown apps** for the app you opened the APK from.

Superseded location: an identical earlier copy exists at `pradeeprai87/bharatamvinyas.com` under `APKs/`; use this repository instead.
