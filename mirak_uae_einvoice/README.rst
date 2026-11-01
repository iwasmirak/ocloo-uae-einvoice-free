Ocloo UAE E-Invoicing (PINT-AE) — Free Trial
============================================

Odoo 22.0 — Community and Enterprise
Version: 22.0.1.0.2
Author: Ocloo
Support: contact@ocloo.tech — WhatsApp +974 6699 9180
Price: Free (limited to 15 documents)
License: OPL-1

UAE electronic invoicing for Odoo: customer invoices and credit notes are generated in the
official Peppol PINT-AE 1.0.4 format (UBL 2.1), checked before they leave Odoo, and handed to
your Accredited Service Provider (ASP), which delivers them on the Peppol network and reports
them to the FTA.

The module depends on ``account`` only. ``l10n_ae`` is supported (its taxes are recognised
automatically) but not required.

Trial edition
-------------

* Works end to end with the simulation provider: accept, reject, alternate and error behaviours.
* Limited to 15 documents in total (documents that reached Sent or Accepted are counted).
* The REST connector to a real Accredited Service Provider is part of the full edition.
* A banner in the settings and on the dashboard shows the remaining quota and the WhatsApp contact.

Features
--------

* PINT-AE XML for tax invoices (380), out-of-scope invoices (480), credit notes (381) and credit
  notes related to exempt or out-of-scope supplies (81).
* VAT categories S, Z, E, O and AE (reverse charge), mapped from your Odoo taxes and editable.
* Line amounts with VAT, gross price, price discount, base quantity, exemption reasons, HS and
  service accounting codes, GTIN.
* The eight transaction-type flags, invoicing period and frequency of billing.
* Foreign currencies: exchange rate to AED (6 decimals), VAT total and total with VAT in AED.
* Credit note reason (BTAE-03) and reference to the original invoice.
* Pre-validation in English and Arabic, each message with the official rule number: the module's
  own checks, the OASIS UBL 2.1 XSD and the PINT-AE 1.0.4 Schematron artefacts (both shipped).
* Statuses Not sent / Ready / Sent / Accepted / Rejected / Error, exchange log, chatter messages,
  automatic retries, mass sending, optional sending on posting.
* Vendor bills from PINT-AE files: supplier from TRN, Peppol ID or name; products from code,
  barcode or name; purchase taxes from the category; totals checked; duplicate UUIDs refused.
* Readiness checker with a weighted score, dashboard, multi-company rules, user and administrator
  groups, English and Arabic (right-to-left) interface.

Requirements
------------

* Odoo 22.0 with Accounting.
* Python ``lxml`` and ``requests``; optional ``saxonche`` for the official Schematron checks.
* An ASP contract and credentials for live exchange (full edition).

Installation
------------

1. Copy the module folder into your addons path and restart Odoo.
2. Update the apps list and install the module.
3. Open Settings > UAE E-Invoicing, fill in the company identifiers and choose a provider.
4. Run the readiness checker, then validate and send a first test invoice.

Notes
-----

* The module is not an Accredited Service Provider; live exchange requires your own ASP contract.
* The generic REST connector posts raw UBL XML and expects JSON. Unusual provider APIs may need a
  small adapter.
* Trial and full editions share the same models: install them in separate databases. An
  installation hook blocks coexistence.

Ocloo — contact@ocloo.tech — WhatsApp +974 6699 9180 — https://ocloo.tech
