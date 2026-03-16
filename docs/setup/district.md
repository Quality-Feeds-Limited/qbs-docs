---
layout: default
title: District
parent: Setup
nav_order: 2
---

# District
{: .no_toc }

Manage districts within each division for precise location classification.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

Districts organise information within a division, supporting client locations, sales territory management, and reporting. Each record contains the parent division, English and Bangla names, geographic coordinates, and an optional website URL.

### Navigation

{: .note }
📍 **Path:** Setup → District

---

## 2. Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated row number. |
| **Division Name** | Parent division (e.g., Dhaka). |
| **En Name** | Official English name of the district. |
| **Bn Name** | Bangla name of the district. |
| **Latitude** | Geographic latitude coordinate. |
| **Longitude** | Geographic longitude coordinate. |
| **URL** | Optional official website link. |

### Action Buttons

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the edit form. |
| **Delete** | Red | Deletes if not used elsewhere. |

---

## 3. Creating a New District

Click **"New District"** in the top-right corner.

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Division Name** | Yes * | Select the parent division (e.g., Dhaka). |
| **English Name** | Yes * | Official English name (e.g., Dhaka). |
| **Bangla Name** | No | Bangla name (e.g., ঢাকা). |
| **Latitude** | No | Geographic latitude coordinate. |
| **Longitude** | No | Geographic longitude coordinate. |
| **URL** | No | Official website URL. |
| **Is Active** | No | Toggle to enable or disable. |

---

## 4. Deletion Policy

Blocked if the district is used in client location setup, sales regions, or any referencing module.

{: .important }
🔒 The system prevents deletion of districts in use.

---

## 5. Related Modules

| Module | Relationship |
|--------|-------------|
| [Division](division) | Each district must be linked to a parent division. |
| [Area](area) | Areas are nested under districts. |
| Customer Management | Clients may be assigned to districts. |
