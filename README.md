---
# Python for Engineering Automation - Portfolio

### Mattia Ricci | Professional Engineer (Mechanical & IXL Signalling)

Welcome to my portfolio. I am a Mechanical and Industrial Engineer specializing in safety-critical railway signalling systems (SIL-4 IXL).

Beyond my core responsibilities, I develop Python automation tools to address process bottlenecks identified during my project work. The tools featured here have saved hundreds of engineering hours, improved data integrity, and reduced project risks. This portfolio provides an overview of these key initiatives.

---

## Tool Showcase

### 1. HMI/Alarm Multilingual Translation System

A desktop application developed to automate the multilingual data workflow for the Brussels Metro Modernisation project.

*   **The Challenge:** The project required translating over 30,000 text strings for the Human-Machine Interface (HMI) from nested JSON files. A manual approach was too slow and created a high risk of data corruption, jeopardizing project schedules.
*   **My Initiative:** I developed a Python application that automates the full translation workflow in two distinct stages:

    1.  **Extraction:** The tool first scans the source kit, extracts all text strings from the JSON files, and records their unique structural path. It then removes duplicates and filters irrelevant data, exporting a clean `.xlsx` file ready for the translation team.

    2.  **Injection:** Once the `.xlsx` file is translated, the tool uses the stored structural paths to inject the new languages back into the correct locations, rebuilding the JSON files.

    This two-stage process automates the full workflow, eliminating manual edits and ensuring the data integrity of the final software kit.

#### Key Features & Impact:
*   **Reduced Engineering Time:** Cut the hands-on engineering work from over a month of manual data handling to **under 5 minutes** of automated processing.
*   **Accelerated Project Workflow:** This automation enabled the entire translation cycle, including external team turnaround, to be completed in a predictable **3-day timeframe**.
*   **Designed for Team Use:** Built with a full Graphical User Interface (GUI), allowing non-technical colleagues to run the data extraction and injection processes independently.
*   **Reliable Architecture:** Developed using an Object-Oriented and multi-threaded design to process large datasets without freezing the user interface and to simplify future maintenance.

#### Visuals:

**Application GUI:**
![GUI Screenshot for the HMI Translation Tool]([INSERT_IMAGE_URL_HERE])

**"Before & After" Data Comparison:**
![Before and After comparison of English and translated Dutch JSON file]([INSERT_IMAGE_URL_HERE])

**Core Code Logic (Recursive Engine):**
![A Python function showing the recursive logic for processing nested JSON data]([INSERT_IMAGE_URL_HERE])```

---

### 2. CBTC/RBC Interface Data Validator & Generator

A foundational data-processing framework designed to automate the validation and generation of the critical data interface between the IXL (Interlocking) and CBTC (Train Control) systems.

*   **The Challenge:** Manually configuring and verifying thousands of data points between the IXL and CBTC systems was a major source of project risk, leading to potential data inconsistencies that were difficult to trace and rectify.
*   **My Initiative:** I engineered a Python solution that embeds critical domain knowledge directly into the workflow. The application automatically reads and connects data from disparate engineering sources—the primary Excel ICDD and the core IXL database files. It then uses a built-in engine of engineering rules to systematically cross-reference every data point, identifying errors and inconsistencies that were nearly impossible to spot manually.

#### Key Features & Impact:
*   **Drastic Error Reduction:** The validation module was fully implemented and successfully **reduced configuration errors and data discrepancies by over 80%** by automatically identifying inconsistencies that were previously found through manual checks.
*   **Sophisticated Data Modeling:** Went beyond simple scripting to build a system of Python classes that accurately represented the complex relationships between different engineering entities.
*   **Architected for Full Automation:** The tool was intentionally designed as a full-cycle solution. Beyond just *finding* errors, it established the complete architectural framework and data model required for the final, revolutionary step: **the one-click generation of the corrected `.DBF` files**, automating the process of writing validated data back into the IXL configuration.
*   **Independent Verification:** Provided an essential, independent verification layer for the end-to-end data workflow, significantly increasing confidence in the final data quality.

#### Visuals:

**Application GUI (Control Panel):**
![GUI Screenshot for the CBTC/RBC Data Tool]([INSERT_IMAGE_URL_HERE])

**Architectural Flowchart:**
![A flowchart showing the data pipeline from Inputs to Process to Outputs]([INSERT_IMAGE_URL_HERE])

**Core Code Logic (Domain Expertise):**
![A Python function showing the logic for handling specific engineering data rules]([INSERT_IMAGE_URL_HERE])

---

### 3. IXL Database Analysis Tool

A suite of data analysis utilities designed to process and enrich core IXL `.DBF` (database) files, transforming them from cryptic, machine-readable formats into user-friendly, human-readable reports.

*   **The Problem:** Core engineering data, vital for analysis and troubleshooting, was stored across dozens of database tables linked only by programmatic IDs. A simple question could require an engineer to manually cross-reference multiple files, a slow, frustrating, and error-prone process that hampered efficiency.
*   **My Initiative:** I developed a Python application that automates this entire data enrichment process. The tool ingests a primary database file, then intelligently queries multiple secondary "lookup" tables to enrich the data with clear, descriptive text. The final output is a single, comprehensive Excel report where all the information is presented in one place.

#### Key Features & Impact:
*   **Data Accessibility:** Transformed raw, cryptic database files into fully contextualized and easy-to-understand Excel reports, making the data accessible to the entire engineering team.
*   **Massive Efficiency Gains:** Eliminated hours of manual data-gathering and cross-referencing, significantly speeding up troubleshooting, data validation, and reporting tasks.
*   **Engineered for Performance:** Built with an efficient processing engine that uses Python dictionaries for rapid in-memory lookups, allowing it to process and enrich tens of thousands of database records in seconds.
*   **Comprehensive Solution:** Designed as a full analysis suite with a tabbed GUI, providing specific processing modules for a wide range of database types (CONENTCO, CONATTR, TCIMSFUN, etc.).

#### Visuals:

**Application GUI (Analysis Dashboard):**
![GUI Screenshot of the IXL Database Analysis Suite]([INSERT_IMAGE_URL_HERE])

**"Before & After" Data Transformation:**
![A side-by-side comparison of a raw DBF file and the enriched Excel report]([INSERT_IMAGE_URL_HERE])

**Core Code Logic (Efficiency Engine):**
![A Python dictionary comprehension used for high-speed data lookups]([INSERT_IMAGE_URL_HERE])

---

### 4. Software Metadata Extractor

A purpose-built utility to automate the tedious but critical process of verifying software component metadata for official kit releases.

*   **The Problem:** Each software release required an engineer to manually inspect the properties of over 500 individual `.exe` and `.dll` files to document their version and build information. This was a 6+ hour, purely manual process that was both a bottleneck and susceptible to human error.
*   **My Initiative:** I developed a Python desktop application that completely automates this task. The tool recursively scans a target directory, interrogates each file using the Windows API to extract its core metadata, and presents the aggregated data in a clean, readable table for immediate review and export.

#### Key Features & Impact:
*   **Massive Time Savings:** Completely eliminated **6+ hours of manual engineering work** for every software release.
*   **Improved Accuracy & Control:** Provided a reliable, repeatable, and error-proof method for version verification, significantly enhancing release quality control.
*   **User-Friendly Interface:** Features a clean GUI with an integrated data table (`Treeview`) that allows the user to filter by file type and review all metadata before generating a report.
*   **Professional-Grade Output:** Generates a clean, automatically formatted `.txt` report with perfectly aligned columns for easy archiving and review.

#### Visuals:

**Application GUI (Data Aggregator):**
![GUI screenshot of the Software Metadata Extractor tool]([INSERT_IMAGE_URL_HERE])

**"Before & After" Workflow:**
![A comparison of the manual, one-by-one properties check vs the automated final report]([INSERT_IMAGE_URL_HERE])

**Core Code Logic (System API Interaction):**
![A Python function showing the use of the win32api library to extract file properties]([INSERT_IMAGE_URL_HERE])
