---
layout: default
title: Bank Branch
parent: Bank / Cash
nav_order: 2
---

# Bank Branch
{: .no_toc }

Define and manage individual branches for each registered bank.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Bank Branch module allows administrators to define the individual branches of banks registered in the system. Each branch is linked to a parent bank and identified by its **Branch Name** and **Routing Number**. Branch records are referenced when setting up Bank Accounts.

### Navigation

{: .note }
📍 **Path:** Accounting → Bank/Cash → Bank Branch

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **Branch Name** | Name of the bank branch (e.g., Uttara, Dhanmondi Branch). |
| **Routing Number** | Unique numeric routing code for fund transfers (e.g., 51515151). |
| **Bank Name** | The parent bank this branch belongs to. |
| **Bank Code** | Code of the parent bank. |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the Branch Edit modal to modify Branch Name, Routing Number, or linked Bank. |

{: .note }
There is no Delete button. Branch records are permanent once created. Contact your system administrator if a branch created in error needs to be removed.

---

## 3. Creating a New Bank Branch

Click **"New Bank Branch"** in the top-right corner.

### Form Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Branch Name** | Yes * | Name of the branch (e.g., "Uttara Branch", "Dhanmondi Branch"). |
| **Routing Number** | Yes * | Unique numeric routing number assigned to this branch (e.g., 51515151). |
| **Select Bank** | No | Select the parent bank from the dropdown. Strongly recommended — links this branch to its bank. |

{: .note }
💡 Always link a branch to its parent bank. Without a bank association, the branch may not be selectable during Bank Account setup.

---

## 4. Editing an Existing Bank Branch

- Locate the branch in the list.
- Click the **yellow Edit button**.
- Modify the required fields.
- Click **Save** to apply changes.

{: .warning }
Editing the Routing Number or linked Bank of a branch already associated with Bank Accounts may affect transaction routing. Review the impact carefully.

---

## 5. Deletion Policy

Branch records cannot be deleted from the interface.

{: .important }
🔒 Contact your QFL Software Engineering Department or system administrator to remove a branch created in error with no linked data.

---

## 6. Routing Number Reference

| Attribute | Details |
|-----------|---------|
| **Definition** | Unique numeric code identifying each branch in fund transfer systems. |
| **Format** | Numeric only. Length varies by bank (8 to 13 digits). |
| **Usage** | Used in Bank Account setup to specify the branch routing for electronic fund transfers. |
| **Uniqueness** | Each branch must have a unique Routing Number. |

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Bank](bank) | Parent record for each Bank Branch. A bank must exist before its branches can be added. |
| [Bank Account](bank-account) | Bank Accounts are linked to a specific Bank Branch. |
| [Bank Transaction Type](bank-transaction-type) | Transaction types are used alongside bank accounts linked to branches. |
