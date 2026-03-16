---
layout: default
title: Business Type
parent: Setup
nav_order: 4
---

# Business Type
{: .no_toc }

Categorise clients and outlets by their nature of business or trade channel.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

Business Types classify clients or outlets based on their nature of business or trade channel. This supports targeted sales strategies, reporting segmentation, and client management. Each record contains a name and optional description (e.g., Modern Trade — five star hotels such as Le Meridian, Radisson).

### Navigation

{: .note }
📍 **Path:** Setup → Business Type

---

## 2. Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated row number. |
| **Name** | Name of the business type (e.g., Modern Trade). |
| **Description** | Optional context or examples for the business type. |

---

## 3. Creating a New Business Type

Click **"New Business Type"** in the top-right corner.

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Name** | Yes * | Name of the business type (e.g., Modern Trade). |
| **Description** | No | Brief description or examples (e.g., Five star hotels such as Le Meridian, Radisson). |
| **Is Active** | No | Toggle to enable or disable. |

{: .note }
💡 Include representative examples in the description to help users correctly classify clients.

---

## 4. Deletion Policy

Blocked if the business type is used in client setup, sales channel configuration, or any referencing module.

---

## 5. Related Modules

| Module | Relationship |
|--------|-------------|
| Customer Management | Clients are classified under a business type during setup. |
| Sales Management | Sales channels may be segmented by business type. |
| Reporting | Business type is used as a filter and grouping dimension in reports. |
