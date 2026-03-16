---
layout: default
title: Division
parent: Setup
nav_order: 1
---

# Division
{: .no_toc }

Manage top-level geographic divisions used across the ERP system.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

Divisions organise and classify information such as client locations, sales territories, reporting structures, and operational regions. Each record contains **English and Bangla names** and an optional website URL.

### Navigation

{: .note }
📍 **Path:** Setup → Division

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Field Name | Description |
|--------|-----------|-------------|
| **SL** | Serial No. | Auto-generated row number. |
| **En Name** | EnName | Official English name of the division. |
| **Bn Name** | BnName | Bangla name of the division. |
| **URL** | Url | Optional official website link. |

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the edit form to modify the division. |
| **Delete** | Red | Deletes the record if not used elsewhere. |

{: .warning }
If a division is already used in other modules, the system will block deletion to protect data integrity.

---

## 3. Creating a New Division

Click **"New Division"** in the top-right corner.

### Form Fields

| Field | Required? | Guidance |
|-------|-----------|----------|
| **English Name** | Yes * | Official English name (e.g., Dhaka). |
| **Bangla Name** | No | Bangla name (e.g., ঢাকা). |
| **URL** | No | Official website URL. |
| **Is Active** | No | Toggle to enable or disable the division. |

{: .note }
💡 Use official government naming conventions for consistency across the system.

---

## 4. Editing an Existing Record

- Locate the division → click **Edit** → update fields → click **Save**.

{: .warning }
Editing the division name may affect how it appears in reports or location-based modules.

---

## 5. Deleting a Record

Deletion is blocked if the division is used in client location setup, sales regions, or any other referencing module.

{: .important }
🔒 The system will prevent deletion and display an error if the division is in use.

---

## 6. Related Modules

| Module | Relationship |
|--------|-------------|
| [District](district) | Each district must be linked to a parent division. |
| Customer Management | Clients may be assigned to divisions based on location. |
| Reporting | Division information is used for regional performance reporting. |
