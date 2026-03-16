---
layout: default
title: Bank
parent: Bank / Cash
nav_order: 1
---

# Bank
{: .no_toc }

Define and manage the master list of banks recognised by the organisation.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Bank module allows administrators to define and manage the list of banks used by the organisation. These records serve as the foundation for creating Bank Accounts and recording bank-related financial transactions. Each bank entry has a **Bank Name** and a unique **Bank Code**.

### Navigation

{: .note }
📍 **Path:** Accounting → Bank/Cash → Bank

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **Bank Name** | Full name of the bank (e.g., DBBL Bank, Sonali Bank Limited). |
| **Bank Code** | Unique alphanumeric identifier (e.g., 0231, SBL001). |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the bank record form to modify Bank Name or Bank Code. |

{: .note }
There is no **Delete** button for Bank records. Once created, bank records are permanent as they may be referenced by Bank Accounts and transactions. Contact your system administrator to remove a record created in error.

---

## 3. Creating a New Bank

Click the green **"New Bank"** button in the top-right corner.

### Required Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Bank Name** | Yes * | Full official name of the bank (e.g., "Brac Bank PLC", "Sonali Bank Limited"). |
| **Bank Code** | Yes * | Unique alphanumeric code (e.g., 054, SBL001, DBBL004). |

Click **Save** to create or **Close** to discard.

{: .note }
💡 Use the bank's official abbreviation followed by a sequence number (e.g., BBL001, DBL002) to make records easy to identify.

---

## 4. Editing an Existing Bank Record

- Locate the bank record in the list.
- Click the **yellow Edit button**.
- Modify Bank Name and/or Bank Code as required.
- Click **Save** to apply changes, or **Close** to discard.

{: .warning }
Editing a bank that is already linked to Bank Accounts or transactions will update the reference across the system. Review the impact carefully before changing records in a live environment.

---

## 5. Deletion Policy

Bank records cannot be deleted from the interface. They are permanent master data.

{: .important }
🔒 If a bank was created in error and has no linked data, contact your QFL Software Engineering Department or system administrator to perform the removal at the database level.

---

## 6. Related Modules

| Module | Relationship |
|--------|-------------|
| [Bank Accounts](bank-account) | Each Bank Account must be linked to a Bank defined here. |
| [Bank Branch](bank-branch) | Bank Branches are created under a specific Bank. The Bank must exist first. |
| [Bank Transaction Type](bank-transaction-type) | Transaction types are used alongside bank accounts to classify GL entries. |
| [Payment](payment) | Payment transactions reference bank accounts linked to a Bank. |
| [Receive](receive) | Receipt transactions reference bank accounts linked to a Bank. |
