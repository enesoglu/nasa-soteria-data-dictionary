# NASA SOTERIA AI Data Explorer

## Overview

The **NASA SOTERIA AI Data Explorer** is an open-source, single-file HTML documentation tool designed to help understand the **content, structure, and semantics of the NASA SOTERIA dataset**.

This repository exists to directly address those searches by clearly explaining **what data exists, where it is located, and how it can be used for AI model development**.

> This project focuses on **dataset comprehension**, not data distribution.

---

## Purpose

The NASA SOTERIA dataset contains large-scale **multimodal physiological, behavioral, and flight telemetry data** collected during high-fidelity pilot simulation experiments.  
While the dataset is extremely valuable for AI research, its raw structure is difficult to interpret due to:

- Deeply nested directory hierarchies
- Thousands of device-specific sensor files
- Binary formats such as `.blob` and `.indicies`
- Aviation- and neuroscience-specific terminology

**NASA SOTERIA AI Data Explorer** was created to solve this problem.

It enables users to quickly:
- Identify **Features (X)** and **Targets (Y)** for machine learning
- Understand each file type and sensor modality
- Navigate the dataset without reading extensive NASA documentation first

---

## What This Repository Contains

This repository contains:

- `index.html` — A standalone, interactive **NASA SOTERIA dataset dictionary**
- Visual explanations of:
  - Folder structure
  - File formats
  - Sensor modalities
  - Processed vs raw data
- AI-oriented semantic tagging of files

This repository **does not contain** the actual NASA SOTERIA data.

---

## Key Features

### 1. Interactive Dataset Structure Explorer

- Mirrors the official NASA SOTERIA directory layout
- Groups thousands of repetitive sensor files into logical components
- Provides per-file explanations directly in the interface

### 2. AI-Centric Data Classification

Each file is categorized based on its role in an AI/ML pipeline:

| Tag | Meaning |
|---|---|
| **TARGET (Y)** | Ground truth labels (e.g., RPSA, NASA-TLX scores, event timestamps) |
| **FEATURE (X)** | Processed metrics usable as model inputs |
| **RAW** | Unprocessed sensor streams and videos |
| **CLEAN** | Quality masks and validation matrices |
| **META** | Documentation, configuration, and manifests |

This directly supports tasks such as:
- Cognitive workload estimation
- Pilot performance modeling
- Stress and attention prediction
- Multimodal time-series learning

---

### 3. Integrated Technical Glossary

The explorer includes a built-in glossary covering common search terms such as:

- EEG workload features
- Heart Rate Variability (HRV)
- Galvanic Skin Response (GSR / EDA)
- Eye-tracking metrics (pupil diameter, gaze vectors)
- Aviation telemetry (PFD, EICAS, cockpit controls)
- File formats: `.blob`, `.indicies`, `.mjpeg`

This makes the dataset accessible even to researchers without an aviation background.

---

## Dataset Structure

The explorer deeply covers NASA SOTERIA dataset contents and it's explanations.

```
Analysis/
  - Model-ready features and labels (CSV, XLSX)

Crew_XX/
  - Individual simulation sessions
  - Subject metadata
  - Synched multimodal recordings

Synched/[Timestamp]/
  - ABM (EEG)
  - Emp_Emp (Physiological Sensors - ECG, GSR, Temperature, Motion)
  - SmartEye (Eye Tracking)
  - IFD_COCKPIT (Flight Telemetry)
  - Instrument Panel Screens
  - Scene Camera (External View Camera)

Processing/
  - Time-aligned CSV files
  - Event vectors
  - Data existence matrices

EventReport/
  - Pilot-written narratives

DVR/
  - Synchronized aircraft instruments, cockpit and external flight videos
```

---

## Technical Details

- Single-file HTML (no backend)
- No build process required
- Works offline
- Open directly in a browser

---

## Disclaimer

- This repository **does not distribute NASA SOTERIA data**
- This is an **unofficial, independent project**
- Not affiliated with or endorsed by NASA
- All information is provided *as is*, users must verify all details against official NASA documentation before use in safety-critical or academic work

---

*NASA SOTERIA dataset content*, *NASA SOTERIA AI data*, *Pilot performance machine learning dataset*, *Aviation safety multimodal dataset*, *EEG ECG flight simulation data*, *NASA cognitive workload dataset*