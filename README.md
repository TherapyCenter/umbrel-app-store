# TherapyCenter Umbrel App Store

Community app store for [umbrelOS](https://umbrel.com) with **[KuentaPOS](https://github.com/TherapyCenter/KuentaPOS)** –
invoicing, cash register and e-invoices for auto repair shops.

## Install

1. In umbrelOS open the **App Store**, click the **⋯** button (top right) → **Community App Stores**.
2. Paste `https://github.com/TherapyCenter/umbrel-app-store` and click **Add**.
3. Open the *TherapyCenter* store and install **KuentaPOS**.

KuentaPOS then runs at `http://umbrel.local:3700`. The data lives on your Umbrel in the app's data folder;
back it up in KuentaPOS under *KuentaPOS → Back up data* as well.

## Updates

The image `ghcr.io/therapycenter/kuentapos` is built by the KuentaPOS repository for every release (amd64 and arm64).
For a new version, `version` in `therapycenter-kuenta/umbrel-app.yml` and the image tag with its digest in
`therapycenter-kuenta/docker-compose.yml` are updated here; umbrelOS then offers the update.
The app ID and folder `therapycenter-kuenta` keep the old name on purpose: changing them would make umbrelOS treat
the app as a new one, without updates for existing installations and without their data.

---

## Deutsch

Community-App-Store für umbrelOS mit **KuentaPOS**. Im App Store über **⋯ → Community App Stores** die Adresse
`https://github.com/TherapyCenter/umbrel-app-store` hinzufügen und KuentaPOS installieren. KuentaPOS läuft danach
unter `http://umbrel.local:3700`; die Daten bleiben auf Ihrem Umbrel.
