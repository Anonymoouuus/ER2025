# *ER2025*

This repository contains the implementation for the paper:

# **A Dual-Faceted Framework for Modeling Temporal Semantic Sequences**
## *Submitted to ER2025*

**Authors:**  
`{first.author, second.author, third.author, fourth.author}@example.com`

---
## Abstract 
Various disciplines model their objects of study as chronological se-
quences of punctual or durable semantic elements. This paper addresses the need
for a standardized framework that can accommodate diverse types of temporal
data and their semantic associations, thus facilitating understanding, reasoning
and communication. Specifically, we introduce a dual-faceted framework that
separates the high-level, user-oriented aspects from the low-level, computational
aspects, thereby establishing a clear bridge between conceptual reasoning and
operational execution in temporal semantic sequence manipulation. Our frame-
work consists of a multidimentional model, a flat one, and a set of transformation
rules that ensure the unification and the consistency of temporal semantic se-
quences with both explicit and implicit temporal information. This framework
also enables the integration of varying temporal formats, facilitating comparative
analyses and supporting the development of cross-domain applications. Through
a running example, we illustrate the framework’s applicability and the advantages
it offers in achieving a more coherent and adaptable representation of temporal
semantic data.
## 📘 Overview

This code provides a concrete implementation of the **dual-faceted framework** introduced in the paper, which models and manipulates **Temporal Semantic Sequences (TSS)** with varying temporal representation.

The framework enables **standardization and integration** of diverse temporal data *(e.g., mobility, weather, communication)*, supporting both **conceptual modeling** and **operational execution**.

---

## 🔑 Key Features

- **Transformation Rules**  
  Handles cases with missing timestamps or durations and completes them using consistent transformation logic.

- **Transformation Process**  
  Combines multiple TSS into a **Flat-Temporal Semantic Sequence (FTSS)** with precise time slicing and semantic merging.

- **Extensible Design**  
  Supports various data types *(mobility, weather, patient records, etc.)* with configurable parameters (e.g., *epsilon*).

---

## 📦 Requirements

- Python ≥ 3.7  
- No external libraries required (uses only **Python standard libraries**)

---


## 🔍 Functions Description

### `transform_to_ftss(data, data_type)`
> Completes missing timestamps or durations in a **Temporal Semantic Sequence (TSS)**.

- **Inputs:**
  - `data`: `list of (timestamp, duration, semantic_set)`
  - `data_type`: one of `'mobility'`, `'weather'`, `'communication'`, `'student'`, `'patient'` *(extendable)*

- **Returns:** Completed TSS

---

### `tss_to_ftss(tss_list)`
> Unifies multiple completed TSS into a single **Flat FTSS** with consistent slices and merged semantics.

- **Input:** `list of completed TSS`
- **Output:** `list of (semantic_set, start_time, duration)`

---

### `decrypt_activity(activity_set, data_type)`
> Maps encoded activities *(e.g., numeric codes in mobility data)* into human-readable labels using a predefined dictionary.

---

## 📚 Examples Covered

From the Paper:

- **Running Example:**  
  *Mobility + Weather + Communication* for `2025-04-01`

- **Table 1:**  
  *Patient records, student tasks, weather reports, daily activity logs*

These demonstrate how the framework adapts to **heterogeneous temporal formats**.

