---
layout: default
title: Bank Account
parent: Bank / Cash
nav_order: 3
---

# Bank Account
{: .no_toc }

Register and manage all company bank accounts in a centralised register.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Bank Account module allows administrators to create, view, and manage all company bank accounts. Each record links a company branch to a specific bank, branch, Chart of Accounts entry, and account type — ensuring accurate reconciliation and financial reporting.

### Navigation

{: .note }
📍 **Path:** Bank/Cash → Bank Accounts

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **Account Name** | Display name for the bank account record. |
| **Account No.** | Official bank account number. |
| **Account Type** | Type of bank account (e.g., Savings, Current). |
| **Bank Name** | The bank associated with this account. |
| **Branch Name** | The specific branch of the selected bank. |
| **Routing No.** | Routing / clearing number auto-filled from the branch. |
| **Current Balance** | Live running balance in the system. |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **View** | Blue | Opens the account in read-only detail view. |
| **Edit** | Yellow / Orange | Opens the account form pre-filled to modify the record. |

---

## 3. Viewing a Bank Account

Click the **blue View button** on the row to open the Bank Account Details screen in read-only mode.

### Details Screen Sections

| Section | Fields |
|---------|--------|
| **Summary Cards** | Current Balance, Opening Balance, Outstanding Balance, Status. |
| **Account Information** | Account Name, Account No., Account Type, Routing Number, Interest Rate, Linked COA. |
| **Bank & Branch** | Bank Name, Bank Code, Branch Name, Branch Routing No., Bank Status. |
| **Contact & Address** | Contact Person, Contact Number, Contact Person 2, Contact Number 2, Address, Remarks. |
| **Audit Information** | Created By, Created At, Updated By, Updated At. |

---

## 4. Creating a New Bank Account

Click the green **"New Bank Account"** button in the top-right corner.

### Step 1 — Select Account Category

| Option | Description |
|--------|-------------|
| **Bank** | For accounts held at a bank institution (default). |
| **Cash** | For petty cash or internal cash accounts. |

### Step 2 — Fill in the Required Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Name** | Yes * | Clear, descriptive name (e.g., HO Main Account). |
| **Select Bank** | Yes * | Choose the bank from the dropdown. |
| **Select Branch** | Yes * | Branches auto-populate based on the selected bank. |
| **Select COA** | No | Chart of Accounts entry to link to the general ledger. |
| **Select Bank Account Type** | Yes * | Account type (e.g., Savings, Current). |
| **Account No** | Yes * | Official bank account number. |
| **Routing Number** | Yes * | Auto-populated when a branch is selected. Can be overridden. |
| **Opening Balance** | Yes * | Initial balance at account setup. Enter 0 if none. |
| **Corporate Supporting Person** | No | Primary contact person for this account. |
| **Contact Number** | No | Primary contact phone number. |
| **Corporate Supporting Person 2** | No | Secondary contact person. |
| **Contact Number 2** | No | Secondary contact phone number. |
| **Company Branch** | Yes * | Associates this account with a specific company branch. |
| **Status** | Yes * | Active = available for transactions. Inactive = hidden from dropdowns. |
| **Address** | No | Physical address of the bank branch or account holder. |
| **Remarks** | No | Additional notes. |

Click **Submit** to create the record.

{: .note }
💡 Prefix accounts by branch — e.g., "HO Main Account" for Head Office — to make filtering easier.

---

## 5. Editing an Existing Record

- Locate the record in the list.
- Click the **yellow Edit button**.
- The Edit form opens pre-filled.
- Modify the required fields.
- Click **Update** to save.

{: .warning }
Editing the Bank, Branch, COA, or Account Type of a record already in use will affect how existing transactions are classified in financial reports.

---

## 6. Deleting a Record

### When Deletion is Allowed
- The account was newly created with no linked transactions.
- Created in error with no associated financial data.

### When Deletion is Blocked
- One or more payment, receipt, or transfer vouchers are posted against this account.

{: .important }
🔒 The system will prevent deletion and display an error if the account has transaction history.

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Bank](bank) | Defines the bank institutions available for selection. |
| [Bank Branch](bank-branch) | Provides the routing number auto-fill for each account. |
| [Bank Transaction Type](bank-transaction-type) | Categories used to classify payment, receipt, and transfer transactions. |
| [Chart of Accounts](../accounting/chart-of-accounts) | The COA entry linked to each bank account determines its GL appearance. |
| [Payment](payment) / [Receive](receive) / [Transfer](transfer) | All transactions reference a Bank Account record for posting. |
