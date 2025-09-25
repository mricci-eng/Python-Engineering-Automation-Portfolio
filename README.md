---
# Python for Engineering Automation - Portfolio

### Mattia Ricci | Professional Engineer (Mechanical & IXL Signalling)

Welcome to my portfolio. I am a Mechanical and Industrial Engineer specializing in safety-critical railway signalling systems (SIL-4 IXL).

Beyond my core engineering duties, I have a proven track record of independently identifying critical process bottlenecks and developing robust Python automation tools to solve them. These tools have saved hundreds of engineering hours, reduced project risk, and improved data quality and consistency. This portfolio provides a high-level showcase of these initiatives.

---

## Tool Showcase

### 1. HMI/Alarm Multilingual Translation System

A robust desktop application developed to support the complex multilingual data requirements of the Brussels Metro Modernisation project.

*   **The Challenge:** The project required the translation of over 30,000 unique, deeply nested JSON strings for the Human-Machine Interface (HMI). A manual approach presented significant risks to the project schedule and data integrity.
*   **My Initiative:** I engineered a standalone Python application that functions as a complete, two-stage data pipeline:
  
    1.  **Extraction & Curation Engine:** The tool first automatically scans the source kit, recursively parsing complex JSON files to extract all text strings and their unique structural paths. It then cleans this data—removing duplicates and irrelevant entries—to produce a single, perfectly structured `.xlsx` file ready for the translation team.
       
    2.  **Intelligent Injection Engine:** After translation, the tool takes the completed `.xlsx` file and uses the stored structural paths to precisely inject the new language data back into the software kit, rebuilding the JSON files while guaranteeing perfect data integrity.

#### Key Features & Impact:
*   **Engineering Time Obliterated:** Reduced the **hands-on engineering effort** for data extraction and integration from over a month of high-risk manual work to **under 5 minutes** of automated processing.
*   **Workflow Revolutionized:** This automation was the key enabler that compressed the entire end-to-end translation workflow, including the external translation team's turnaround, into a predictable **3-day cycle**, a timeline that was previously impossible.
*   **Engineered for Usability:** Features a full Graphical User Interface (GUI) built with ttkbootstrap, enabling non-developer team members to execute the translation workflow safely and efficiently.
*   **Robust & Scalable:** Architected using Object-Oriented principles and a multi-threaded design to handle long-running operations without compromising user experience, making the tool adaptable for future projects.

#### Visuals:

**Application GUI:**
![GUI Screenshot for the HMI Translation Tool]([INSERT_IMAGE_URL_HERE])

**"Before & After" Data Comparison:**
![Before and After comparison of English and translated Dutch JSON file]([INSERT_IMAGE_URL_HERE])

**Core Code Logic (Recursive Engine):**
![A Python function showing the recursive logic for processing nested JSON data]([INSERT_IMAGE_URL_HERE])

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
