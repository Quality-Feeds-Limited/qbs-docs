---
layout: default
title: Bank Transaction Type
parent: Bank / Cash
nav_order: 4
---

# Bank Transaction Type
{: .no_toc }

Define classification types for bank and cash transactions, linked to GL Voucher Types.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Bank Transaction Type module allows administrators to define and manage the classification types used for bank and cash transactions. Each transaction must be assigned a type, which determines how it is categorised and linked to the appropriate GL Voucher Type.

### Navigation

{: .note }
📍 **Path:** Accounting → Bank/Cash → Bank Transaction Type

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **Voucher Type** | The GL voucher type linked to this transaction type (e.g., Receipt Voucher, Payment Voucher). |
| **Name** | Descriptive name of the transaction type (e.g., Receipt, Payment). |
| **Code** | Unique alphanumeric identifier (e.g., RCPT-0001, PMT-0002). |
| **Purpose** | Purpose category: **Receipt**, **Payment**, or **Transfer**. |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the form to modify the existing record. |
| **Delete** | Red | Removes the record — only if not used in any bank transaction. |

{: .warning }
The **Delete** button will be blocked if the type is already assigned to one or more bank transactions.

---

## 3. Creating a New Bank Transaction Type

Click **"New Bank Transaction Type"** in the top-right corner.

### Form Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Name** | Yes * | Clear, descriptive name (e.g., "Receipt", "Bank Payment"). |
| **Code** | No | Optional unique alphanumeric code (e.g., RCPT-0001). |
| **Select Purpose** | No | Choose: **Receipt**, **Payment**, or **Transfer**. |
| **GL Voucher Type** | Yes * | Select the appropriate GL voucher type (e.g., Receipt Voucher — RV, Payment Voucher — PV, Contra Voucher — CV). |

{: .note }
💡 Prefix Receipt types with `RCPT-` and Payment types with `PMT-` for easy filtering and reporting.

---

## 4. Editing an Existing Record

- Click the **yellow Edit button** on the row.
- The Edit modal opens pre-filled.
- Modify the required fields.
- Click **Save** to apply changes.

{: .warning }
Editing the Name, Code, Purpose, or GL Voucher Type of a type already in use will affect how existing bank transactions are classified and posted to the GL.

---

## 5. Deleting a Record

### When Deletion is Allowed
- The type is newly created with no linked transactions.

### When Deletion is Blocked
- The type is assigned to one or more bank or cash transactions.

{: .important }
🔒 The system will prevent deletion and show an error if the type is in use.

**Steps to delete:** locate the record → click **red Delete** → confirm deletion.

---

## 6. Purpose & GL Voucher Type Reference

| Purpose | GL Voucher Type | Typical Use | Code Example |
|---------|----------------|-------------|--------------|
| **Receipt** | Receipt Voucher (RV) | Money received from customers or income sources | RCPT-0001 |
| **Payment** | Payment Voucher (PV) | Money paid to suppliers, employees, or expenses | PMT-0002 |
| **Transfer** | Contra Voucher (CV) | Internal transfer between bank or cash accounts | TRF-0003 |

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Payment](payment) | Uses Bank Transaction Type to classify outgoing payments and link to GL. |
| [Receive](receive) | Uses Bank Transaction Type to classify incoming receipts. |
| [Transfer](transfer) | Uses Bank Transaction Type with Transfer purpose for inter-account movements. |
| [General Ledger](../accounting/general-ledger) | Transactions post to GL through the voucher type linked to each transaction type. |
