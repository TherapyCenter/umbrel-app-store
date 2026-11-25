# TherapyCenter Umbrel App Store

Community app store for [umbrelOS](https://umbrel.com) with **[OpenWerkstatt](https://github.com/TherapyCenter/OpenWerkstatt)** –
invoicing, cash register and e-invoices for auto repair shops. OpenWerkstatt is open source (GNU AGPL 3.0) and all
features are free.

## Install

1. In umbrelOS open the **App Store**, click the **⋯** button (top right) → **Community App Stores**.
2. Paste `https://github.com/TherapyCenter/umbrel-app-store` and click **Add**.
3. Open the *TherapyCenter* store and install **OpenWerkstatt**.

OpenWerkstatt then runs at `http://umbrel.local:3700`. The data lives on your Umbrel in the app's data folder;
back it up in OpenWerkstatt under *OpenWerkstatt → Back up data* as well.

## Updates

umbrelOS offers an update as soon as a new OpenWerkstatt version is in this store. The update notice inside OpenWerkstatt is
switched off on Umbrel (`OPENWERKSTATT_UPDATE_CHECK: "0"` in `docker-compose.yml`), so it does not point to versions
that are not in the store yet.

For maintainers, for every OpenWerkstatt release:

1. Wait until the OpenWerkstatt repository has built the image `ghcr.io/therapycenter/openwerkstatt:<version>`
   (amd64 and arm64, workflow *Container image*).
2. `therapycenter-openwerkstatt/umbrel-app.yml`: set `version` and write the `releaseNotes`.
3. `therapycenter-openwerkstatt/docker-compose.yml`: set the image to `ghcr.io/therapycenter/openwerkstatt:<version>@sha256:<digest>`
   (digest of the multi-platform image, e.g. from the summary of the workflow run).
4. Do not delete an image from the registry while this store still points to it.

Do not change the app ID and folder `therapycenter-openwerkstatt`: umbrelOS would treat the app as a new one,
without updates for existing installations and without their data.

The screenshots come from the OpenWerkstatt repository (`docs/screenshots/`), the icon from `public/img/icon.svg` there.

## Screenshots

![Invoice](https://raw.githubusercontent.com/TherapyCenter/OpenWerkstatt/main/docs/screenshots/1-invoice.png)

![Receipt](https://raw.githubusercontent.com/TherapyCenter/OpenWerkstatt/main/docs/screenshots/2-receipt.png)

![Swiss QR-bill](https://raw.githubusercontent.com/TherapyCenter/OpenWerkstatt/main/docs/screenshots/3-qr-bill.png)

---

## Deutsch

Community-App-Store für umbrelOS mit **[OpenWerkstatt](https://github.com/TherapyCenter/OpenWerkstatt)** – Rechnungen,
Kasse und E-Rechnung für Kfz-Werkstätten. OpenWerkstatt ist Open Source (GNU AGPL 3.0), alle Funktionen sind kostenlos.

**Installieren:** Im App Store über **⋯ → Community App Stores** die Adresse
`https://github.com/TherapyCenter/umbrel-app-store` hinzufügen, den Store *TherapyCenter* öffnen und OpenWerkstatt
installieren. OpenWerkstatt läuft danach unter `http://umbrel.local:3700`. Die Daten bleiben auf Ihrem Umbrel im
Datenordner der App; sichern Sie sie zusätzlich in OpenWerkstatt unter *OpenWerkstatt → Daten sichern*.

**Updates:** umbrelOS bietet ein Update an, sobald eine neue OpenWerkstatt-Version in diesem Store steht. Der
Update-Hinweis in OpenWerkstatt selbst ist auf Umbrel abgeschaltet.
