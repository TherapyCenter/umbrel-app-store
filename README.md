# TherapyCenter Umbrel App Store

Community app store for [umbrelOS](https://umbrel.com) with **[Kuenta](https://github.com/TherapyCenter/Kuenta)** –
invoicing, cash register and e-invoices for auto repair shops.

## Install

1. In umbrelOS open the **App Store**, click the **⋯** button (top right) → **Community App Stores**.
2. Paste `https://github.com/TherapyCenter/umbrel-app-store` and click **Add**.
3. Open the *TherapyCenter* store and install **Kuenta**.

Kuenta then runs at `http://umbrel.local:3700`. The data lives on your Umbrel in the app's data folder;
back it up in Kuenta under *Kuenta → Back up data* as well.

## Updates

The image `ghcr.io/therapycenter/kuenta` is built by the Kuenta repository for every release (amd64 and arm64).
For a new version, `version` in `therapycenter-kuenta/umbrel-app.yml` and the image tag with its digest in
`therapycenter-kuenta/docker-compose.yml` are updated here; umbrelOS then offers the update.

---

## Deutsch

Community-App-Store für umbrelOS mit **Kuenta**. Im App Store über **⋯ → Community App Stores** die Adresse
`https://github.com/TherapyCenter/umbrel-app-store` hinzufügen und Kuenta installieren. Kuenta läuft danach
unter `http://umbrel.local:3700`; die Daten bleiben auf Ihrem Umbrel.
