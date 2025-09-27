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

<!-- Side/By side Table (two images - Single row) -->
<!-- APPLICATION GUI -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="2">
        <b>Application GUI</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Trasl_GUI_1.JPG?raw=true" alt="GUI_1" width="800">
      </td>
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Trasl_GUI_2.JPG?raw=true" alt="GUI_2" width="800">
      </td>
    </tr>
  </table>
</p>

<!-- Two rows table -->
<!-- BEFORE AND AFTER (ENG_FR / ENG_NL) -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td>
        <b>"Before & After" Data Comparison</b>
      </td>
    </tr>
    <!-- This row holds the two stacked images -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/json_eng_fr.png?raw=true" alt="ENG_FR" width="700">
        <br>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/json_eng_nl.png?raw=true" alt="ENG_NL" width="700">
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- NESTED JSON RECURSIVE FUNCTION -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Core Code Logic (Recursive Nested JSON Function)</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Trasl_nested_Json.png?raw=true" alt="Nested JSON Function" width="500">
      </td>
    </tr>
  </table>
</p>

---

### 2. CBTC/IXL Interface Data Validator & Generator

A Python tool to automate the validation of the IXL-to-CBTC data interface, ensuring data integrity before implementation.

*   **The Challenge:** Manual configuration of the data interface between the IXL (Interlocking) and CBTC (Train Control) systems was a source of errors that were time-consuming to find and correct.
*   **My Initiative:** I developed a Python application that automates these validation checks. The tool ingests and cross-references data from the two main sources, CBTC `.xlsx` data and the core IXL database (`.DBF`) files. It uses an object-oriented data model and a rule-based engine to compare the expected configuration against the as-built IXL database, automatically flagging discrepancies.

#### Key Features & Impact:
*   **Reduced Configuration Errors:** The validation engine reduced data configuration errors by **over 80%**, identifying mismatches that were previously caught only by manual review.
*   **Automated Cross-Referencing:** Replaced a time-consuming manual check process by automatically comparing data across multiple, complex engineering documents.
*   **Designed for Full Automation:** The application was architected to create a closed-loop configuration process. Its next planned feature was to use the validated data model to automatically populate the final IXL configuration databases (`.DBF` files) based upon the previously CBTC validated data. This would have replaced the high-risk manual data entry stage, ensuring that the final system configuration perfectly matched the verified engineering design.
*   **Improved Data Integrity:** Provided a reliable and repeatable method to verify the quality and consistency of the IXL/CBTC interface data before deployment.

#### Visuals:

<!-- Single Image table -->
<!-- GUI -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Application GUI (Control Panel)</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Rel_GUI.JPG?raw=true" alt="ID_TIPOENT91 ICDD Filling Sample" width="700">
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- LOGIC SAMPLE -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Architectural Flowchart</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Rel_Tool_Flowchart.png?raw=true" alt="Flowchart" width="300">
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- LOGIC SAMPLE -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Core Code Logic (Domain Expertise)</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/CBTC_IXL_example_logic.JPG?raw=true" alt="ID_TIPOENT91 ICDD Filling Sample" width="400">
      </td>
    </tr>
  </table>
</p>

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

<!-- Single Image table -->
<!-- APPLICATION GUI -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Application GUI</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/ext_DBFs_GUI.png?raw=true" alt="Ext DBFs GUI" width="500">
      </td>
    </tr>
  </table>
</p>


<!-- Two rows table -->
<!-- BEFORE AND AFTER (CRYPT / EXT) -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td>
        <b>"Before & After" Data Comparison</b>
      </td>
    </tr>
    <!-- This row holds the two stacked images -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/Attr_encr.JPG?raw=true" alt="encrypted dbf" width="200">
        <br>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/extended_attr_SANITIZED.JPG?raw=true" alt="ext dbf" width="800">
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- CORE LOGIC -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Core Code Logic:</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://github.com/mricci-eng/Python-Engineering-Automation-Portfolio/blob/main/images/ext_core_logic.png?raw=true" alt="Ext DBFs Core Logic" width="500">
      </td>
    </tr>
  </table>
</p>

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
