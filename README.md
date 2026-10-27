# Quran TV — Admin Panel

A single-file static admin dashboard for the Quran TV app. Built with vanilla HTML/CSS/JS
and the Firebase Web SDK (compat build) for authentication and Firestore.

## Pages

- `index.html` — the admin panel (served at the site root)
- `admin.html` — identical copy, same panel

## Setup

1. Open `index.html`.
2. Replace the placeholder `firebaseConfig` object near the bottom of the file with your own
   Firebase web config (Firebase Console -> Project Settings -> General -> Your apps).
3. In Firebase Console -> Authentication -> Users, add an admin user manually with the
   email/password provider enabled.
4. Make sure your Firestore security rules only allow your admin account to read/write the
   `videos`, `categories`, `feedback` and `users` collections.

## Hosting

Served with GitHub Pages from the `main` branch root.

## Warning

This is a fully client-side app. Anyone can read the source and see your Firebase web config
(that is normal and safe for Firebase web apps — the config is not a secret). Your real
security boundary is Firestore rules plus Firebase Auth, so lock those down before going live.
