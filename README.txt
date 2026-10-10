TAKASH WHATSAPP v3 — PHONE AUTHENTICATION PROTOTYPE

WHAT THIS VERSION DOES
- Sign in with a phone number using Firebase SMS verification and reCAPTCHA.
- Saves a basic profile in Firestore under users/{uid}.
- Provides a shared community chat using the Firestore messages collection.
- This is a web prototype, not an Android APK and not yet a private one-to-one messaging app.

IMPORTANT BEFORE TESTING
1. Host this app on an HTTPS website. Opening index.html directly from Downloads (file://) will not work for Firebase phone verification.
2. In Firebase Console > Authentication > Settings, add your hosting domain under Authorized domains.
3. Authentication > Sign-in method: ensure Phone is enabled.
4. Confirm SMS region policy allows Malawi (+265).
5. Firestore test mode is not safe for a public app. Do not launch publicly until Firestore Security Rules restrict access. The demo uses the `users` and `messages` collections.
6. Firebase phone verification may have SMS quotas/costs. Use Firebase Authentication test phone numbers while developing if available.

NEXT STEP
Choose a hosting service that lets you upload index.html from your phone (for example, a static HTTPS host). Then add its exact domain to Firebase Authentication > Settings > Authorized domains. Never share account passwords or SMS verification codes.

This project uses the Firebase JavaScript SDK via Google's CDN. The Firebase web configuration is included to connect this prototype to the configured project; database security must be enforced with Firebase rules.
