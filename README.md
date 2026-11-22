<p align="center">
  <a href="https://github.com/Bjeffrey85/FreeTube-Android-app/releases/latest">
    <img width="160" height="160" alt="FreeTube" src="https://github.com/user-attachments/assets/bf6f0313-26b6-4a97-87c5-cd0285c71638" />
  </a>
</p>

<h1 align="center">FreeTube for Android</h1>

<p align="center">
  <b>YouTube in its own sandboxed app.</b><br>
  Your Google login lives here and nowhere else on your phone.
</p>

<p align="center">
  <a href="https://github.com/Bjeffrey85/FreeTube-Andriod-app/releases">
    <img alt="Download APK" src="https://img.shields.io/badge/Download-APK-14b8a6?style=for-the-badge&logo=android&logoColor=white" />
  </a>
</p>

---

FreeTube is a stripped-down browser that can only open YouTube. Sign in to your Google account here and your regular browser stays signed out, so YouTube's tracking stays out of the rest of your browsing.

It runs on **GeckoView**, Firefox's own engine packaged as an app, not Android's WebView. That means Google sign-in works, your login sticks, and real Firefox extensions run inside it.

## Features

- **Stays signed in.** Cookies are saved in a normal Firefox profile in the app's private storage. There's no private mode, nothing is cleared when you close the app, and Android backups are off.
- **YouTube only.** Only YouTube and Google sign-in pages open inside the app. Any other link opens in your normal browser instead.
- **Background play.** Audio keeps going with the screen off or while you use other apps.
- **Media controls.** Play, pause, next and previous work from the notification shade, the lock screen and Bluetooth headphones.
- **Ad-free.** uBlock Origin is built in, and SponsorBlock skips sponsor segments.
- **Locked down.** Camera, microphone, location and notification requests are blocked. HTTPS-only mode and Global Privacy Control are on.
- **Behaves like an app.** Fullscreen video rotates to landscape, Back goes back a page, and the app pauses for phone calls and when you unplug headphones.
- **Opens YouTube links.** Set it as the app for YouTube links and they open here.

## Install

1. Download **[FreeTube-Android.apk](https://github.com/Bjeffrey85/FreeTube-Android-app/releases)** to your phone.
2. Open it and allow your browser or file manager to install apps.
3. Open FreeTube and tap **Allow** when it asks about notifications. The background-play controls need this.
4. Sign in to YouTube.

The first launch takes a few seconds while the extensions install.

**Open YouTube links in FreeTube:** go to Settings → Apps → FreeTube → Open by default → Add links.

> ⚠️ Don't use **Clear storage** on FreeTube in Android settings. That's where your login is saved. **Clear cache** is fine.

## Requirements

- Android 8.0 or newer
- 64-bit ARM phone (nearly every phone since 2019)
- Works on GrapheneOS

## Build from source

1. Install [Android Studio](https://developer.android.com/studio) and open this folder.
2. Let the first sync finish. It downloads the Android SDK, Gradle and GeckoView.
3. Choose **Build → Select Build Variant → release**.
4. Choose **Build → Generate App Bundles or APKs → Generate APKs**.

The APK is written to `app/build/outputs/apk/release/`.

To update the Firefox engine, set `geckoviewVersion` in `app/build.gradle.kts` to the newest version listed [here](https://maven.mozilla.org/maven2/org/mozilla/geckoview/geckoview/maven-metadata.xml) and rebuild.

## Desktop version

FreeTube for Windows is at **[Bjeffrey85/FreeTube](https://github.com/Bjeffrey85/FreeTube)**.

## Credits

- [GeckoView](https://firefox-source-docs.mozilla.org/mobile/android/geckoview/) by Mozilla
- [uBlock Origin](https://github.com/gorhill/uBlock) by Raymond Hill
- [SponsorBlock](https://sponsor.ajay.app/) by Ajay Ramachandran
- [Video Background Play Fix](https://addons.mozilla.org/firefox/addon/video-background-play-fix/) by Tim Chien
