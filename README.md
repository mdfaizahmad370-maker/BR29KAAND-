# BR29KAAND PROMOTIONS — Flutter Android starter

A polished Flutter starter for the BR29KAAND PROMOTIONS booking app. It includes a runnable customer-facing UI, service selection, a multi-field booking form, booking list/status cards, WhatsApp/Instagram/email launch links, and deployment scaffolding for Firebase + Razorpay + WhatsApp Business Platform.

## Important status
This is a **starter project, not a verified production release**. It has not been built or tested on an Android device in this environment. Firebase, Razorpay, WhatsApp Business, FCM, legal policies, and signing credentials must be configured before real bookings/payments or publication. The app UI currently uses local demo state; do not accept real payments from it.

## Run locally
1. Install Flutter stable and Android Studio.
2. Run `flutter create .` from this folder if platform folders are missing.
3. Replace `pubspec.yaml` with the included one or merge its dependencies.
4. Run `flutter pub get`.
5. Run `flutter run`.
6. To configure Firebase, install FlutterFire CLI and run `flutterfire configure`; add the generated `firebase_options.dart`, then wire the services in `lib/`.

## Business details
- Business: BR29KAAND PROMOTIONS
- Instagram: https://www.instagram.com/br29kaand/
- WhatsApp: +917632870122
- Email: mdfaizahmad370@gmail.com
- Currency: INR
- Owner-set prices only; no fixed prices or guaranteed results.

## Production checklist
- Configure Firebase Authentication, Firestore, Storage, Cloud Functions, and FCM.
- Set owner/admin role from a trusted backend process only; never from public registration.
- Deploy `firestore.rules` and `storage.rules`.
- Implement server-side booking creation, offer acceptance, and status transition validation.
- Implement Razorpay order creation and signature/webhook verification in Cloud Functions. Keep secret keys only in server secrets.
- Configure WhatsApp Business Platform and approved templates; collect appropriate opt-in.
- Add privacy policy, terms, cancellation/refund policy, data deletion flow, and support SLA.
- Run tests, dependency/security review, accessibility checks, and device testing.
- Configure app ID, app icon, signing keys, versioning, and Play Console disclosures.
- Build: `flutter build apk --debug` for testing; `flutter build appbundle --release` for Play upload after signing setup.

## Security note
Never treat the client UI or a payment-success callback as proof of payment. Only a verified backend event may mark a payment as confirmed.

## Build APK in the cloud (without installing Flutter locally)
1. Upload this project to a GitHub repository.
2. Open the repository's **Actions** tab and select **Build Android APK**.
3. Press **Run workflow** (or push to `main`).
4. When the workflow finishes successfully, open the workflow run and download the `br29kaand-promotions-debug-apk` artifact.
5. Extract the artifact ZIP to get `app-debug.apk` and install it on an Android test device.

This creates a **debug/test APK**, not a signed Play Store release. The current app is demo-mode; do not use it to collect real customer bookings or payments until backend integrations are completed and tested.
