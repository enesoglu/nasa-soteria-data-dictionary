🚀 NASA SOTERIA AI Data Explorer

An interactive, web-based data dictionary and file navigator designed to demystify the NASA SOTERIA (System-Wide Safety and Assurance Technologies for Aviation) dataset for AI researchers and data scientists.

📖 Overview

The NASA SOTERIA dataset contains massive amounts of multimodal physiological and flight telemetry data collected during pilot simulation sessions. However, its raw directory structure involves thousands of nested files, complex naming conventions (e.g., Emp_Acc.blob, ABM.indicies), and aviation-specific acronyms that can be overwhelming for machine learning practitioners.

NASA SOTERIA AI Data Explorer bridges this gap. It is a single-file HTML tool that visualizes the dataset structure, explains every file format, and defines technical terms, enabling researchers to quickly identify Features (X) and Targets (Y) for their models.

✨ Key Features

🔍 1. Interactive File Tree with Virtual Grouping

Smart Hierarchy: Instead of listing thousands of repetitive sensor log files, the explorer intelligently groups them into logical "Virtual Folders" (e.g., Empatica E4, ABM EEG, Instrument Panel).

Format Explanations: Hovering over or clicking a file (like .blob or .indicies) reveals exactly what data it holds (e.g., "Binary raw microvolt signals").

🏷️ 2. Semantic Data Tagging

Color-coded badges instantly categorize files based on their utility in an AI pipeline:

<span style="color:#166534; background:#dcfce7; padding:2px 6px; border-radius:4px;">TARGET (Y)</span> : Ground truth labels (e.g., RPSA scores, Event timestamps).

<span style="color:#6b21a8; background:#f3e8ff; padding:2px 6px; border-radius:4px;">FEATURE (X)</span> : Processed input metrics (e.g., Workload Index, Heart Rate Variability).

<span style="color:#1e40af; background:#dbeafe; padding:2px 6px; border-radius:4px;">RAW</span> : Unprocessed sensor data (e.g., .blob streams, video files).

<span style="color:#9a3412; background:#ffedd5; padding:2px 6px; border-radius:4px;">CLEAN</span> : Quality masks and existence matrices for data filtering.

📚 3. Integrated Aviation & Physiology Glossary

A built-in glossary defines critical domain terms, ensuring you know the difference between:

Physiological Metrics: GSR (Galvanic Skin Response), HRV (Heart Rate Variability), Pupil Diameter.

Flight Telemetry: PFD (Primary Flight Display), EICAS, Yoke Inputs, G-Load.

Cognitive States: WorkloadFBDS, Engagement Index, Distraction.

⚡ 4. Live Search & Filtering

Instantly search for specific file extensions (e.g., .csv), sensor names (e.g., SmartEye), or concepts.

The tree structure automatically expands to show relevant results.

📂 Understanding the Dataset Structure

The explorer visualizes the standardized folder structure used in the SOTERIA project:

Analysis/: Contains high-level CSVs used for modeling (Labels & Features).

Crew_XX/: Root folder for specific flight sessions.

Synched/[Timestamp]/: The core data folder containing time-synchronized recordings.

ABM/: EEG (Brainwave) data.

Emp_Emp/: Wristband biosignals (Acc, Bvp, Gsr, Temp).

SmartEye/: Eye-tracking and gaze vectors.

IFD_COCKPIT/: Flight telemetry (Speed, Altitude, Controls).

scenecamera/ & inst panel/: Video recordings of the cockpit.

Processing/: Intermediate CSV files generated from raw binaries.

EventReport/: Pilot narratives describing anomalies or errors.

DVR/: Integrated over-the-shoulder flight videos.

🛠️ Technology Stack

HTML5: Semantic structure.

Tailwind CSS (CDN): Modern, responsive styling.

Vanilla JavaScript: Logic for tree rendering, search, and language switching.

FontAwesome (CDN): Icons for file types and UI elements.

Single-File Architecture: The entire tool lives in one index.html file for easy sharing and deployment.

🚀 How to Use

Download the NASA_SOTERIA_Data_Explorer.html file.

Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

Use the Sidebar to switch between the File Explorer and Glossary.

Use the Search Bar to find specific data types.

🗝️ Keywords & Tags

NASA SOTERIA, Aviation Safety, Human Factors, Pilot Performance Dataset, Physiological Data, EEG Analysis, ECG/EKG, Heart Rate Variability (HRV), Galvanic Skin Response (GSR), Eye Tracking, SmartEye, ABM B-Alert, Empatica E4, Flight Simulation, Machine Learning, Data Dictionary, Metadata Explorer, Cognitive Workload, Safety-II, X-Plane, Telemetry.

⚠️ Disclaimer

This tool is a documentation and visualization aid created to assist researchers in understanding the NASA SOTERIA dataset structure. It does not contain the actual dataset files (which are terabytes in size). It strictly visualizes the metadata and hierarchy.