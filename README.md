# Ocloo UAE E-Invoicing (PINT-AE) — Free Trial

UAE electronic invoicing for Odoo. Customer invoices and credit notes are generated in the
official **Peppol PINT-AE 1.0.4** format (UBL 2.1), validated before they leave Odoo, and handed
to a service provider for delivery on the Peppol network.

This repository holds the **free trial** of the module for Odoo 17, 18, 19, 20, 21 and 22.

## What the trial does

* PINT-AE XML for tax invoices (380), out-of-scope invoices (480), credit notes (381) and
  credit notes for exempt supplies (81), with VAT categories S, Z, E, O and AE, the eight
  transaction-type flags, AED totals for foreign currencies and payment means.
* Pre-validation before sending: the module's own business checks, the OASIS UBL 2.1 XSD and the
  official PINT-AE 1.0.4 Schematron rules, each message with its rule number, in English and Arabic.
* A simulation provider to test the whole flow: accept, reject, alternate and error behaviours.
* Vendor bill import from supplier PINT-AE files, with duplicate detection.
* Readiness checker with a weighted score, a dashboard, exchange logs, retries and mass sending.
* English and Arabic (right-to-left) interface, user and administrator groups, multi-company rules.

## Limits of the trial

* **15 documents in total** — documents that reached *Sent* or *Accepted* are counted.
* The **REST connector to a real Accredited Service Provider is not available** in this edition.
  The full edition removes the quota and enables that connector.

## Branches

Each Odoo series has its own branch, with the module folder at the root:

| Branch | Odoo | Module |
|---|---|---|
| [`17.0`](../../tree/17.0) | 17.0 | `mirak_uae_einvoice` |
| [`18.0`](../../tree/18.0) | 18.0 | `mirak_uae_einvoice` |
| [`19.0`](../../tree/19.0) | 19.0 | `mirak_uae_einvoice` |
| [`20.0`](../../tree/20.0) | 20.0 | `mirak_uae_einvoice` |
| [`21.0`](../../tree/21.0) | 21.0 | `mirak_uae_einvoice` |
| [`22.0`](../../tree/22.0) | 22.0 | `mirak_uae_einvoice` |

Ready-to-install archives are attached to the [latest release](../../releases/latest).

## Installation

1. Download the ZIP for your Odoo version, or clone the matching branch.
2. Copy the `mirak_uae_einvoice` folder into your addons path and restart Odoo.
3. Update the apps list and install **Ocloo UAE E-Invoicing (PINT-AE) — Free Trial**.
4. Open *Settings → UAE E-Invoicing*: TRN, Peppol participant ID, trade licence, emirate, mandate date.
5. Choose the simulation provider, run the readiness checker, then post, validate and send an invoice.

Requirements: the `account` module, Python `lxml` and `requests`; optional `saxonche` for the
official Schematron validation.

## Tests

The Odoo 19 suite of this edition runs 37 tests with no failure, including the quota gate and the
connector restriction. Modules for the other series are verified statically (Python compilation,
XML well-formedness, manifest and asset checks).

## Full edition

Unlimited documents, the configurable REST connector for your Accredited Service Provider,
participant lookup and live status follow-up. The full edition is distributed separately.

## Contact

Ocloo — contact@ocloo.tech — WhatsApp [+974 6699 9180](https://wa.me/97466999180) — https://ocloo.tech

License: OPL-1 (Odoo Proprietary License v1.0). © 2026 Ocloo.
