# Kayseri Şehir Hastanesi – Privacy Policy

This repository hosts the privacy policy of the **Kayseri Şehir Hastanesi** mobile application, published by T.C. Sağlık Bakanlığı and developed by KEYDATA BİLGİ İŞLEM TEKNOLOJİ SİSTEMLERİ A.Ş.

The policy is a single static page (`index.html`) served with GitHub Pages at:

**https://medricscorp.github.io/kayseri-sehir-hastanesi-privacy/**

The page contains the policy in three languages. The part of the URL after `#` selects the language:

| Language | URL |
|----------|-----|
| Türkçe   | https://medricscorp.github.io/kayseri-sehir-hastanesi-privacy/#tr |
| English  | https://medricscorp.github.io/kayseri-sehir-hastanesi-privacy/#en |
| العربية  | https://medricscorp.github.io/kayseri-sehir-hastanesi-privacy/#ar |

If no language is given, the page uses the browser's language (English if it is not Turkish or Arabic).

## Why it exists

Google Play requires every app that handles personal or sensitive user data to publish a privacy policy. The policy must be:

- available at a working, public URL (not a PDF, and not behind a login),
- linked from the store listing, and
- reachable from inside the app.

The Kayseri app handles personal data (Turkish ID number, name, phone number, appointments, location during indoor navigation), so it needs this policy. The page explains what the app collects, why, who it is shared with, and how users can use their rights under KVKK (Law No. 6698).

## Where it is used

1. **Inside the Android app.** A "Privacy Policy" link on the **sign-in screen** and the **profile edit screen** opens this page in the app's current language. The URLs are set in the `privacy_policy_url` string in:
   - `app/src/main/res/values/strings.xml` (`#tr`)
   - `app/src/main/res/values-en/strings.xml` (`#en`)
   - `app/src/main/res/values-ar/strings.xml` (`#ar`)
2. **Google Play Console.** The "Privacy policy" field of the store listing (App content → Privacy policy) points to this URL. Google reviewers check it during app review.
3. **App Store Connect (iOS).** The iOS app can use the same URL in its "Privacy Policy URL" field.

## Why this repository is public

- **Users must be able to read the policy without an account.** Anyone who taps the link in the app, or opens it from the store page, must see it. That includes people with no GitHub account and Google or Apple reviewers.
- **GitHub Pages needs it.** On the GitHub Free plan, a Pages site can only be published from a public repository.
- **There is nothing secret here.** The repository holds only the policy text, which is meant to be public anyway.

## Why it must stay public

**Do not make this repository private, rename it, delete it, or turn off GitHub Pages.** Any of these makes the URL stop working or become restricted, and then:

- the in-app "Privacy Policy" link opens an error page (404),
- the Play Store listing points to a dead link, which breaks Google Play's User Data policy,
- Google can reject new app updates, or remove the app from the store, until a working policy URL is restored.

Even on a paid GitHub plan, a Pages site from a private repository can be limited to organization members. That breaks public access in the same way.

If the URL ever has to change, update the app strings above, release a new app version, and update the URL in Play Console (and App Store Connect) **before** the old URL stops working.

## Updating the policy

1. Edit `index.html`. Keep the three languages (`data-lang="tr"`, `"en"`, `"ar"`) in sync, so each one says the same thing.
2. Update the **effective date** in all three languages.
3. Keep the `#tr`, `#en` and `#ar` anchors working, because the app links to them.
4. Commit to the default branch. GitHub Pages republishes the site automatically, usually within a few minutes.
5. When the app starts collecting new data or uses a new third-party service, update this policy **and** the Data safety form in Play Console at the same time.

**Do not put any secrets, credentials, internal notes or personal data in this repository.** Everything here is publicly visible.

## Related

- Konya Şehir Hastanesi uses the same structure: https://medricscorp.github.io/konya-sehir-hastanesi-privacy/
- Contact for policy questions: info@keydata.com.tr
