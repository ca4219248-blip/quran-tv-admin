# Quran TV - Admin Panel

A single-file static admin dashboard for the Quran TV app, built with vanilla HTML/CSS/JS and
the Firebase Web SDK (compat build) for authentication and Firestore.

## Files

- `index.html` - the admin panel, served at the site root
- `admin.html` - identical copy of the same panel

## Setup

1. Open `index.html`.
2. Replace the placeholder `firebaseConfig` object near the bottom of the file with your own
   Firebase web config (Firebase Console -> Project Settings -> General -> Your apps).
3. In Firebase Console -> Authentication -> Users, add an admin user manually with the
   email/password provider enabled.
4. Lock down Firestore security rules so only your admin account can read/write the
   `videos`, `categories`, `feedback` and `users` collections.

## Hosting

Served with GitHub Pages from the `main` branch root.

## Note on security

This is a fully client-side app. Anyone can view the source and see your Firebase web config.
That is normal and safe for Firebase web apps - the web config is not a secret. Your real
security boundary is Firebase Authentication plus Firestore security rules, so configure
those before sharing the URL.
