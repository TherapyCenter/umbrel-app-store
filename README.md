# TherapyCenter Umbrel App Store

Community app store for [umbrelOS](https://umbrel.com) with **[KuentaPOS](https://github.com/TherapyCenter/KuentaPOS)** –
invoicing, cash register and e-invoices for auto repair shops. KuentaPOS is open source (GNU AGPL 3.0) and all
features are free.

## Install

1. In umbrelOS open the **App Store**, click the **⋯** button (top right) → **Community App Stores**.
2. Paste `https://github.com/TherapyCenter/umbrel-app-store` and click **Add**.
3. Open the *TherapyCenter* store and install **KuentaPOS**.

KuentaPOS then runs at `http://umbrel.local:3700`. The data lives on your Umbrel in the app's data folder;
back it up in KuentaPOS under *KuentaPOS → Back up data* as well.

## Updates

umbrelOS offers an update as soon as a new KuentaPOS version is in this store. The update notice inside KuentaPOS is
switched off on Umbrel (`KUENTAPOS_UPDATE_CHECK: "0"` in `docker-compose.yml`), so it does not point to versions
that are not in the store yet.

For maintainers, for every KuentaPOS release:

1. Wait until the KuentaPOS repository has built the image `ghcr.io/therapycenter/kuentapos:<version>`
   (amd64 and arm64, workflow *Container image*).
2. `therapycenter-kuenta/umbrel-app.yml`: set `version` and write the `releaseNotes`.
3. `therapycenter-kuenta/docker-compose.yml`: set the image to `ghcr.io/therapycenter/kuentapos:<version>@sha256:<digest>`
   (digest of the multi-platform image, e.g. from the summary of the workflow run).
4. Do not delete an image from the registry while this store still points to it.

The app ID and folder `therapycenter-kuenta` keep the old name on purpose: changing them would make umbrelOS treat
the app as a new one, without updates for existing installations and without their data.

The screenshots come from the KuentaPOS repository (`docs/screenshots/`), the icon from `public/img/icon.svg` there.

## Screenshots

![Invoice](https://raw.githubusercontent.com/TherapyCenter/KuentaPOS/main/docs/screenshots/1-invoice.png)

![Receipt](https://raw.githubusercontent.com/TherapyCenter/KuentaPOS/main/docs/screenshots/2-receipt.png)

![Swiss QR-bill](https://raw.githubusercontent.com/TherapyCenter/KuentaPOS/main/docs/screenshots/3-qr-bill.png)

---

## Deutsch

Community-App-Store für umbrelOS mit **[KuentaPOS](https://github.com/TherapyCenter/KuentaPOS)** – Rechnungen,
Kasse und E-Rechnung für Kfz-Werkstätten. KuentaPOS ist Open Source (GNU AGPL 3.0), alle Funktionen sind kostenlos.

**Installieren:** Im App Store über **⋯ → Community App Stores** die Adresse
`https://github.com/TherapyCenter/umbrel-app-store` hinzufügen, den Store *TherapyCenter* öffnen und KuentaPOS
installieren. KuentaPOS läuft danach unter `http://umbrel.local:3700`. Die Daten bleiben auf Ihrem Umbrel im
Datenordner der App; sichern Sie sie zusätzlich in KuentaPOS unter *KuentaPOS → Daten sichern*.

**Updates:** umbrelOS bietet ein Update an, sobald eine neue KuentaPOS-Version in diesem Store steht. Der
Update-Hinweis in KuentaPOS selbst ist auf Umbrel abgeschaltet.
