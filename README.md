# Integration guide for PartnerJam

Hello, welcome to the integration guide for PartnerJam! This guide will help you integrate your Shopify app with PartnerJam, enabling you to launch your partnership program in no time. Integration consists of one simple step: you need to include a snippet of PartnerJam code in your app's codebase. This allows us to perform attribution when a new referral is installed via your publisher's link.

## How it works

When someone clicks the referral link, we create a fingerprint of their device. After the installation, our snippet creates another fingerprint and compares it with all other records in the database. If there's a match, we attribute the installation to the publisher whose fingerprint matched the one created after the installation. The attribution window is 60 days by default.

## How to integrate with PartnerJam

Follow the [integration guide here](./docs/ATTRIBUTION.md).
