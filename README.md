<p align="center">
  <img src="./docs/imgs/hyperswitch-logo-dark.svg#gh-dark-mode-only" alt="Hyperswitch-Logo" width="40%" />
  <img src="./docs/imgs/hyperswitch-logo-light.svg#gh-light-mode-only" alt="Hyperswitch-Logo" width="40%" />
</p>

<h1 align="center">Composable Open-Source Payments Infrastructure</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/juspay/hyperswitch/main/docs/gifs/quickstart.gif" alt="Quickstart demo" />
</p>

<p align="center">
  <a href="https://github.com/juspay/hyperswitch/actions?query=workflow%3ACI+branch%3Amain">
    <img src="https://github.com/github/docs/actions/workflows/main.yml/badge.svg" alt="CI Status" />
  </a>
  <a href="https://github.com/juspay/hyperswitch/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/juspay/hyperswitch" alt="License" />
  </a>
  <img src="https://img.shields.io/badge/Made_in-Rust-orange" alt="Made in Rust" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/company/hyperswitch/">
    <img src="https://img.shields.io/badge/follow-hyperswitch-blue?logo=linkedin&labelColor=grey" alt="LinkedIn" />
  </a>
  <a href="https://x.com/hyperswitchio">
    <img src="https://img.shields.io/badge/follow-%40hyperswitchio-white?logo=x&labelColor=grey" alt="X/Twitter" />
  </a>
  <a href="https://inviter.co/hyperswitch-slack">
    <img src="https://img.shields.io/badge/chat-on_slack-blue?logo=slack&labelColor=grey&color=%233f0e40" alt="Slack" />
  </a>
</p>

---

## 📖 Table of Contents
* [Why Hyperswitch?](#-why-hyperswitch)
* [Payment Modules](#-payment-modules)
* [Getting Started](#-getting-started)
  * [Local Setup (Docker)](#1-local-setup-via-docker)
  * [Hosted Sandbox](#2-hosted-sandbox-no-setup)
  * [Cloud Deployment](#3-cloud-deployment)
* [Architecture](#-architectural-overview)
* [Community & Contributing](#-community--contributing)
* [License](#-license)

---

## ⚡ Why Hyperswitch?

Hyperswitch is a commercial open-source payments stack purpose-built for scale, flexibility, and developer experience. Often referred to as the **“Linux for Payments,”** it serves as a well-architected reference for teams who want to truly own their payments stack.

Built in **Rust** for maximum performance and reliability, Hyperswitch lets you pick only the components you need—whether it’s routing, retries, vaulting, or observability—without vendor lock-in or bloated integrations. 

* **Open Source by Default:** Transparency drives trust and builds better, reusable software.
* **Embrace Payment Diversity:** Support for global payment methods (cards, wallets, BNPL, UPI, Pay by Bank).
* **Enterprise-Tested:** Maintained by Juspay, the team powering payment infrastructure for 400+ leading enterprises worldwide.

---

## 🧩 Payment Modules

Hyperswitch offers a modular design. Pick and integrate only the modules you need on top of your existing payment stack:

* **[Intelligent Routing](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/intelligent-routing):** Route each transaction to the PSP with the highest predicted auth rate to minimize latency and maximize success.
* **[Revenue Recovery](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/revenue-recovery):** Combat passive churn with intelligent retry strategies tuned by card bin, region, and method.
* **[Vault](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/vault):** A PCI-compliant vault service to store cards, tokens, wallets, and bank credentials securely.
* **[Cost Observability](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/ai-powered-cost-observability):** Detect hidden fees, downgrades, and penalties with self-serve dashboards.
* **[Reconciliation](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/reconciliation):** Automate 2-way and 3-way reconciliation with backdated support and customizable outputs.
* **[Alternate Payment Methods](https://docs.hyperswitch.io/about-hyperswitch/payments-modules/enable-alternate-payment-method-widgets):** Drop-in widgets for Apple Pay, Google Pay, PayPal, Klarna, and more.

---

## 🚀 Getting Started

Choose the deployment method that works best for you.

### 1. Local Setup via Docker
Get Hyperswitch running on your local machine in minutes. 

```bash
# Clone the repository
git clone --depth 1 --branch latest [https://github.com/juspay/hyperswitch](https://github.com/juspay/hyperswitch)
cd hyperswitch

# Run the setup script
scripts/setup.sh
