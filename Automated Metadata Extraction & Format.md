# Automated Metadata Extraction & Formatting Process

This document outlines the automated workflows for ingesting digital assets into Preservica and/or designated networked drives. The process is facilitated by an automated script (`archival-metadata-utility-tool.py`) that can be executed via a Graphical User Interface (GUI) or a Command Line Interface (CLI).

To accommodate read-only environments and write-blocked drives, the script requires all outputs to be directed to a separate, user-specified export directory rather than saving directly to the source drive.

---

## Pre-Requisites & Environment Setup

* **Project Files:** Ensure that you have access to the networked drive **OMCSERV**.
* **Source Connection:** Mount the source device containing the digital assets in **read-only mode** using a physical or software write-blocker.
* **Execution:** You can launch the tool by navigating double-clicking on the archival-metadata-utility-tool.py. Using command line is not advised.

---

## Option 1: Digital Assets Will Be Ingested **With Metadata** to Repository

Use this option when extracting technical metadata directly from a source device of digital assets and the assets have not yet been ingested into Preservica or any other repository with a unique identifier for each asset.

### 1. Metadata Extraction

The script natively extracts metadata by recursively traversing the target directory.

* Hidden directories and files (those starting with a `.`) are ignored to prevent clutter.
* The script captures the Top Level Folder Name, File Name, File Path, Size (Bytes), Creation Date, Format Type, and an empty Author/Creator field.

### 2. Output and Mapping

The script creates a target output directory, copies the Excel template, and names it `<Folder_Name>_Metadata.xlsx`. It maps raw properties extracted from the source to Dublin Core standard fields.

* **Dates:** Converted to the ISO 8601 standard format (`YYYY-MM-DD`).
* **Format and Type:** The script matches file extensions to MIME types and DCMI Types.
* **Specific Mappings:**
    * Folders and archives (`zip`, `tar`, `compressed`, `rar`) map to **Collection**.
    * Applications like `csv`, `excel`, `spreadsheet`, and `spreadsheetml` map strictly to **Dataset**.
    * Text apps (`pdf`, `msword`, `wordprocessingml`, `rtf`, `epub`, `document`) map to **Text**.
    * Software apps (`executable`, `software`) map to **Software**.
    * Files starting with `image/` map to **Image**, `audio/` to **Sound**, and `video/` to **MovingImage**.

### 3. Generate Descriptive Metadata

The script will pause its execution and prompt the user to manually input descriptive metadata.

* User opens the newly generated `<Folder_Name>_Metadata.xlsx` file in the export directory using the **Open File** button or by navigating to the folder.
* User completes the required fields in the "DC" tab (e.g., Contributor, Description, Subject(s), Title).
* User saves and closes the workbook and clicks OK in the GUI to resume execution of the script.
* **Resume Feature:** If there a is a need to pause the project, the excel is saved by the user and they will close out of the utility tool. Opening the utility file again with the same file will detect the existing workbook and offer to resume, preserving your manual edits.

### 4. Data Validation and Export

Once resumed, the script automatically validates the manually entered text.

* **Typo Correction:** The "Title", "Description", "Subject", "Contributor", and "Creator" fields are validated against the "Controlled_Vocabulary" tab. It uses fuzzy matching (>85% similarity) to detect typos and correct them to the institutional standard.
* **Date Validation:** Date fields are checked to ensure they parse correctly into the `YYYY-MM-DD` format.
* **Final Output:** The script exports a fully validated Excel file and a final `DC.csv` file into the designated export directory. The CSV will contain no formulas, macros, or miscellaneous worksheets. If the **OPEX Export** checkbox is selected (or `--opex` flag is supplied in CLI), it also generates Preservica OPEX metadata XML file(s) (`.opex`).

### 5. Ingest Assets

Upload the digital assets and the accompanying `DC.csv` file for the top-level folder to Preservica or the designated networked drive.

---

## Option 2: Digital Assets Ingested **Without Metadata** (Adding IDs Later)

Use this option when extracting technical metadata from a source device and merging it with existing Preservica Entity Reference IDs for assets that have already been ingested into Preservica or any other repository with a unique identifier for each asset.

### 1. Retrieve Preservica Data

User downloads the Preservica export CSV for the ingested assets that contains a title/file name column and an Entity Reference ID column.

### 2. Execution and Extraction

Run the script selecting Option 2, providing the source device path, the Preservica CSV, and an export output directory. The script will extract raw metadata from the source folder identically to Option 1.

### 3. Entity ID Merging

The script automatically matches assets to their Preservica records.

* It performs lookups by matching variations of the file name (exact, without extensions, URL unquoted) against the Preservica export's title column.
* A new column for "Entity Ref" is dynamically added to the metadata template and populated with the matched IDs.

### 4. Manual Entry, Validation, and Export

* The script pauses for manual descriptive metadata entry in the output workbook.

Once resumed, the script automatically validates the manually entered text.

* **Typo Correction:** The "Title", "Description", "Subject", "Contributor", and "Creator" fields are validated against the "Controlled_Vocabulary" tab. It uses fuzzy matching (>85% similarity) to detect typos and correct them to the institutional standard.
* **Date Validation:** Date fields are checked to ensure they parse correctly into the `YYYY-MM-DD` format.
* **Final Output:** The script exports a fully validated Excel file and a final `DC.csv` file into the designated export directory. The CSV will contain no formulas, macros, or miscellaneous worksheets.

---

## Option 3: Technical Metadata Existing

Use this option when technical metadata already exists in an Excel or CSV file, but requires merging with Preservica IDs and descriptive cleanup.

### 1. Required Inputs

Run the script selecting Option 3. You must provide:

* The path to the **Existing Metadata File**.
* The path to the **Preservica CSV**.
* The destination **Export Output Directory**.

### 2. Processing

* **Data Loading:** The script bypasses live folder extraction and instead loads the raw metadata from the provided existing file.
* **Merging & Formatting:** It maps raw properties extracted from the source to Dublin Core standard fields.
* **Dates:** Converted to the ISO 8601 standard format (`YYYY-MM-DD`).
* **Format and Type:** The script matches file extensions to MIME types and DCMI Types.
* **Specific Mappings:**
    * Folders and archives (`zip`, `tar`, `compressed`, `rar`) map to **Collection**.
    * Applications like `csv`, `excel`, `spreadsheet`, and `spreadsheetml` map strictly to **Dataset**.
    * Text apps (`pdf`, `msword`, `wordprocessingml`, `rtf`, `epub`, `document`) map to **Text**.
    * Software apps (`executable`, `software`) map to **Software**.
    * Files starting with `image/` map to **Image**, `audio/` to **Sound**, and `video/` to **MovingImage**.

### 3. Manual Entry, Validation, and Export

* The script pauses for manual descriptive metadata entry in the output workbook.

Once resumed, the script automatically validates the manually entered text.

* **Typo Correction:** The "Title", "Description", "Subject", "Contributor", and "Creator" fields are validated against the "Controlled_Vocabulary" tab. It uses fuzzy matching (>85% similarity) to detect typos and correct them to the institutional standard.
* **Date Validation:** Date fields are checked to ensure they parse correctly into the `YYYY-MM-DD` format.
* **Final Output:** The script exports a fully validated Excel file and a final `DC.csv` file into the designated export directory. The CSV will contain no formulas, macros, or miscellaneous worksheets.

---

## Option 4: Resume Prior Job / Validate Existing Metadata

Use this option to resume an interrupted process or validate an existing metadata Excel file directly without requiring a source directory scan.

### 1. Required Inputs

Run the script selecting Option 4. You must provide:

* The destination **Export Output Directory** (containing the `<Folder_Name>_Metadata.xlsx` file), OR.
* Path to a specific **Existing Metadata File**.

### 2. Validation and Export

* The script preserves any existing manual metadata entries in the `DC` tab.
* **Typo Correction:** The script validates the "Title", "Description", "Subject", "Contributor", and "Creator" fields against the controlled vocabulary.
* **Date Validation:** Date fields are checked to ensure they parse correctly into the `YYYY-MM-DD` format.
* The script outputs the final validated Excel file and `DC.csv` to the designated export directory.
