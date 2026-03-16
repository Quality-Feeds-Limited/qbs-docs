---
layout: default
title: Chart of Accounts
parent: Accounting
nav_order: 2
---

# Chart of Accounts
{: .no_toc }

Define and manage the complete hierarchical list of General Ledger accounts.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Chart of Accounts module provides a structured, hierarchical listing of all GL accounts used by the organisation to record financial transactions. Each account belongs to an Account Type and can be designated as a **Parent Account** (grouping) or a **Child Account** (transaction-level). The screen displays records in **Tree View** by default, visually representing parent-child relationships.

### Purpose
- Define and maintain the complete list of GL accounts.
- Organise accounts in a hierarchical parent-child structure.
- Assign each account to an Account Type (e.g., Asset, Liability, Income, Expense).
- Optionally associate accounts with a specific Branch for branch-level reporting.

### Navigation

{: .note }
📍 **Path:** Accounting → Accounts → Chart of Accounts

---

## 2. Understanding the Screen

### View Controls

| Control | Function |
|---------|----------|
| **Tree View** | Toggles hierarchical layout showing parent-child relationships. |
| **Expand** | Reveals all child accounts beneath each parent. |
| **Collapse** | Hides child accounts, showing only top-level parents. |
| **Page Size Selector** | Controls how many records are shown per page (default: 100). |

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **Chart Of Account Name** | Account name. Parent accounts show a teal **Parent** badge. |
| **Code** | Unique alphanumeric account code (e.g., A-00001). |
| **Account Type** | High-level classification (Asset, Liability, Income, Expense). |
| **Parent** | Name of the parent account. Shows `--` for root-level parents. |

### Tree View Indicators

| Indicator | Meaning |
|-----------|---------|
| Teal **Parent** badge | Grouping account — cannot be used for direct transaction posting. |
| **--** (minus) icon | Parent node is expanded; child accounts are visible. |
| **+** (plus) icon | Parent node is collapsed; child accounts are hidden. |
| Indented row (no badge) | Child account — transaction-level, can be selected in voucher entries. |
| `--` in Parent column | Root-level parent with no parent of its own. |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the Edit modal pre-filled with current values. |
| **Delete** | Red | Removes the account — only if not used in any GL voucher entries and has no child accounts. |

{: .warning }
The **Delete** button will be disabled if the account is used in GL voucher entries or has child accounts beneath it.

---

## 3. Creating a New Account

Click the green **"+ New Chart Of Accounts"** button in the top-right corner to open the Add modal.

### Form Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Account Name** | Yes * | Full descriptive name (e.g., "Cash", "Accounts Receivable"). |
| **Account Code** | Yes * | Unique alphanumeric code following your coding convention (e.g., A-00001). |
| **Account Type** | Yes * | Select classification from dropdown — options drawn from Chart of Accounts Type. |
| **Is Parent Account** | No | Toggle ON to designate as a Parent Account. Hides the Parent Account field when enabled. |
| **Parent Account** | No | Visible when Is Parent Account is OFF. Select the parent to nest this account under. Leave blank for root-level. |
| **Select Branch** | No | Associate this account with a specific branch. If blank, applies to all branches. |

{: .note }
💡 Create all **Parent Accounts** first, then create Child Accounts and link them. This ensures a clean hierarchy from the start.

Click **Save** to create, or **Cancel** to discard.

---

## 4. Editing an Existing Account

Click the **yellow Edit button** on the row. The Edit modal opens pre-filled with current values. The same fields as the Add modal are available. Click **Update** to apply changes or **Cancel** to discard.

{: .warning }
Editing the **Account Type** or **Parent Account** of an account already used in GL voucher entries will affect how existing transactions are classified in financial reports. Review the impact carefully before making changes in a live environment.

---

## 5. Parent and Child Account Structure

### Parent Accounts
- Grouping accounts that aggregate the balances of all child accounts beneath them.
- Marked with the teal **Parent** badge in the list.
- Cannot themselves have a parent — always root-level nodes.
- **Cannot be directly selected in GL voucher entry lines.** Only child accounts can be used for transaction posting.

### Child Accounts
- Transaction-level accounts used directly in GL voucher entries, bank transactions, and other records.
- Must be linked to a Parent Account (or left as root-level).
- Appear indented beneath their parent in Tree View.
- Can only have one parent at a time.

### Example Hierarchy

| Level | Account Name | Code | Account Type | Parent |
|-------|-------------|------|-------------|--------|
| Parent | Accounts Receivable | A-00001 | Asset | -- |
| Parent | Fixed Asset | A-00004 | Asset | -- |
| Child | Vehicle | A-00005 | Asset | Fixed Asset |
| Child | Laptop | A-00009 | Asset | Fixed Asset |
| Parent | Current Asset | A-00006 | Asset | -- |
| Child | Cash | A-00002 | Asset | Current Asset |
| Child/Parent | Bank | A-00003 | Asset | Current Asset |

---

## 6. Deleting an Account

### When Deletion is Allowed
- The account has never been used in any GL voucher entry line.
- The account has no child accounts linked beneath it.

### When Deletion is Blocked
- The account has been used in one or more GL voucher entries.
- The account has one or more child accounts.
- The account is referenced in Bank Account configuration.

{: .important }
🔒 **System Rule:** The system will prevent deletion and display an error message if the account is in use or has child accounts.

---

## 7. Account Code Convention

| Account Type | Code Prefix | Example Codes |
|-------------|------------|---------------|
| Asset | A- | A-00001, A-00002 |
| Liability | L- | L-00001, L-00002 |
| Equity | E- | E-00001 |
| Income / Revenue | I- | I-00001, I-00002 |
| Expense | EX- | EX-00001, EX-00002 |

{: .note }
💡 Use zero-padded numeric suffixes (e.g., A-00001) to ensure correct sorting order in reports and dropdowns.

---

## 8. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts Type](chart-of-accounts-type) | Defines account classifications used in the Account Type field. |
| [General Ledger](general-ledger) | Voucher entry lines reference accounts from the Chart of Accounts. |
| [Bank Accounts](../bank-cash/bank-account) | Bank accounts reference a specific GL account for posting. |
| [Financial Year](financial-year) | Financial reports aggregate GL entries by account using this hierarchy. |
| [Voucher Type](voucher-type) | Voucher types post to GL accounts defined here. |
