---
layout: default
title: Area
parent: Setup
nav_order: 3
---

# Area
{: .no_toc }

Manage areas within each district for the most granular location classification.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

Areas provide fine-grained location classification within a district, supporting precise client locations, sales territory management, and operational zone reporting. Each record contains the parent district, area name, a unique area code, and an optional description.

### Navigation

{: .note }
📍 **Path:** Setup → Area

---

## 2. Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated row number. |
| **District Name** | Parent district (e.g., Dhaka). |
| **Name** | Official name of the area (e.g., Uttara). |
| **Area Code** | Unique code for the area (e.g., A-0001). |
| **Description** | Optional context or notes about the area. |

---

## 3. Creating a New Area

Click **"New Area"** in the top-right corner.

| Field | Required? | Guidance |
|-------|-----------|----------|
| **District Name** | Yes * | Select the parent district (e.g., Dhaka). |
| **Name** | Yes * | Official name of the area (e.g., Uttara). |
| **Area Code** | Yes * | Unique code (e.g., A-0001). |
| **Description** | No | Additional notes or context. |
| **Is Active** | No | Toggle to enable or disable. |

{: .note }
💡 Use a consistent area code format (e.g., A-0001, A-0002) for easy identification and sorting.

---

## 4. Deletion Policy

Blocked if the area is used in client location setup, sales territory configuration, or any referencing module.

---

## 5. Related Modules

| Module | Relationship |
|--------|-------------|
| [District](district) | Each area must be linked to a parent district. |
| [Division](division) | Areas inherit the division hierarchy through their parent district. |
| Customer Management | Clients may be assigned to areas. |
| Sales Management | Sales territories may use area data for granular assignment. |
