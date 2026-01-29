---
# Python for Engineering Automation - Portfolio

### Mattia Ricci | Professional Engineer (Mechanical & IXL Signalling)

Mechanical & Industrial Engineer specializing in SIL-4 IXL systems (Metro/CBTC, Mainline/ERTMS L2).

This portfolio showcases custom Python automation tools I engineered to resolve critical workflow bottlenecks encountered during major international railway projects. These tools were developed to ensure data integrity, accelerate V&V activities, and automate complex brownfield integrations.

---

## Tool Showcase

### 1. HMI/Alarm Multilingual Translation System

**Project:** Brussels Metro Modernisation (Brownfield)

Engineered and deployed a standalone Python application to automate the multilingual translation workflow for the HMI and Alarm systems.

*   The project required the translation of approximately **30,000 text strings** nested within complex JSON files. A manual approach was unfeasible due to the volume of data and the high risk of corrupting the file structure.
*   I developed a two-stage automation pipeline using Object-Oriented Programming (OOP) and a custom GUI:
    1.  **Extraction:** The tool first scans the source kit, extracts all text strings from the (`.JSON`) files, and records their unique structural path. It then removes duplicates and filters irrelevant data, exporting a clean (`.xlsx`) file ready for the translation team.
    2.  **Injection:** Once the (`.xlsx`) file is translated, the tool uses the stored structural paths to inject the new languages back into the correct locations, rebuilding the JSON files.

#### Key Features & Impact:
*   **Process Optimization:** Reduced the total translation processing cycle from **1 month to 3 days**.
*   **Data Integrity:** Eliminated configuration errors caused by manual data entry, ensuring valid JSON structure in the final delivery.
*   **Operational Usability:** Built with a user-friendly GUI (Tkinter/ttkbootstrap), allowing the tool to be operated independently by non-technical team members.
*   **Scalability:** Implemented using multi-threading to handle large datasets efficiently without freezing the user interface.

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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Trasl_GUI_1.JPG?raw=true" alt="GUI_1" width="800">
      </td>
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Trasl_GUI_2.JPG?raw=true" alt="GUI_2" width="800">
      </td>
    </tr>
  </table>
</p>

<!-- Side/By side Table (two images - Single row) -->
<!-- APPLICATION GUI -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="2">
        <b>Before & After" Data Comparison</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/json_eng_fr.png?raw=true" alt="ENG_FR" width="600">
      </td>
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/json_eng_nl.png?raw=true" alt="ENG_NL" width="600">
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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Trasl_nested_Json.png?raw=true" alt="Nested JSON Function" width="500">
      </td>
    </tr>
  </table>
</p>

---

### 2. CBTC/IXL Interface Data Validator & Generator

A Python tool to ensure the integrity of the interface between the Interlocking (IXL) and Train Control (CBTC) systems before implementation.

*   The interface configuration required aligning thousands of data points between the IXL database and the CBTC design specifications. The manual verification process was time-intensive and prone to human error, leading to potential safety-critical mismatches.
*   I architected an object-oriented Python application to automate cross-referencing. The tool creates a digital model of the interface by ingesting data from disparate sources (CBTC-(`.xlsx`) design specs and DBF IXL-(`.DBF`) files) and applying a rule-based engine to verify compliance between the design and the as-built IXL configuration.

#### Key Features & Impact:
*   **Reduced Configuration Errors:** Engineered a solution that eliminated the most common sources of configuration errors between the IXL and CBTC systems.
*   **Data Reliability:** Significantly improved data consistency and reliability for the Brussels Metro interface compared to manual verification methods.
*   **Designed for Full Automation:** The application was architected to create a closed-loop configuration process. Its next planned feature was to use the validated data model to automatically populate the final IXL configuration databases (`.DBF` files) based upon the previously CBTC validated data. This would have replaced the high-risk manual data entry stage, ensuring that the final system configuration perfectly matched the verified engineering design.
*   **Technical Implementation:** Utilized Object-Oriented Programming to map railway entities to Python classes, allowing for scalable data handling across different project version configurations.

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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Rel_GUI.JPG?raw=true" alt="ID_TIPOENT91 ICDD Filling Sample" width="600">
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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Rel_Tool_Flowchart.png?raw=true" alt="Flowchart" width="300">
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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/CBTC_IXL_example_logic.JPG?raw=true" alt="ID_TIPOENT91 ICDD Filling Sample" width="400">
      </td>
    </tr>
  </table>
</p>

---

### 3. IXL Database Analysis Tool

A suite of data analysis utilities designed to process and enrich core IXL `.DBF` (database) files, transforming them into user-friendly, human-readable reports.

*   Core IXL data is stored across decentralized database tables linked only by numerical IDs. Troubleshooting required manual cross-referencing between multiple files, which was inefficient and restricted data accessibility.
*   Engineered a tool to automate the cross-referencing process. The application converts raw data into user-friendly reports by programmatically linking primary database records with secondary lookup tables, injecting human-readable descriptions into the final output.

#### Key Features & Impact:
*   **Accelerated Troubleshooting:** Significantly accelerated the analysis of engineering data by eliminating manual cross-referencing.
*   **Improved Data Accessibility:** Converted cryptic raw data into readable `.xlsx` reports, making the database structure accessible to the wider engineering team.
*   **Performance Engineering:** Utilized Python dictionary hash maps for in-memory lookups, enabling the processing of tens of thousands of records in seconds.
*   **Comprehensive Solution:** Designed as a full analysis suite with a tabbed GUI, providing specific processing modules for a wide range of DBF databases.

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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/ext_DBFs_GUI.png?raw=true" alt="Ext DBFs GUI" width="500">
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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/Attr_encr.JPG?raw=true" alt="crypt DBF source" width="200">
        <br>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/extended_attr_SANITIZED.JPG?raw=true" alt="Ext DBF" width="800">
      </td>
    </tr>
    <!-- This is the Confidentiality Note Row -->
    <tr align="center">
      <td>
        <em>Note: Data shown is representative and has been sanitized to protect client confidentiality.</em>
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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/ext_core_logic.png?raw=true" alt="Ext DBFs Core Logic" width="500">
      </td>
    </tr>
  </table>
</p>

---

### 4. Software Metadata Extractor

A purpose-built utility to automate the tedious but critical process of verifying software component metadata for official kit releases.

*   Each software release required the manual verification of metadata for hundreds individual software components (`.exe` and `.dll`). This process was a bottleneck that consumed significant engineering hours and was prone to human error.
*   Developed a desktop application that automates extraction. The tool interacts with the Windows API to retrieve version and build information from the target directory, aggregating the data into a structured interface for review and reporting.

#### Key Features & Impact:
*   **Improved Accuracy & Control:** Provided a reliable, repeatable, and error-proof method for version verification, significantly enhancing release quality control.
*   **User-Friendly Interface:** Features a clean GUI with an integrated data table (`Treeview`) that allows the user to filter by file type and review all metadata before generating a report.
*   **Professional-Grade Output:** Generates a clean, automatically formatted `.txt` report with perfectly aligned columns for easy archiving and review.

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
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/exelist_gui1.JPG?raw=true" alt="GUI_1" width="800">
      </td>
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/exelist_gui2.JPG?raw=true" alt="GUI_2" width="800">
      </td>
    </tr>
    <!-- This is the Confidentiality Note Row -->
    <tr align="center">
      <td colspan="2">
        <em>Note: Windows System32 folder has been chosen as example path to protect client confidentiality.</em>
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- EXELIST REPORT -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>TXT Report</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/exelist_report.JPG?raw=true" alt="exelist report" width="500">
      </td>
    </tr>
  </table>
</p>

<!-- Single Image table -->
<!-- CORE EXELIST LOGIC MS API INTERACTION -->
<p align="center">
  <table>
    <!-- This is the Title Row -->
    <tr align="center">
      <td colspan="1">
        <b>Core Code Logic (System API Interaction)</b>
      </td>
    </tr>
    <!-- This is the Image Row -->
    <tr align="center">
      <td>
        <img src="https://raw.githubusercontent.com/mricci-eng/Python-Engineering-Automation-Portfolio/main/images/exelist_corelogic.JPG?raw=true" alt="exelist core logic" width="500">
      </td>
    </tr>
  </table>
</p>
