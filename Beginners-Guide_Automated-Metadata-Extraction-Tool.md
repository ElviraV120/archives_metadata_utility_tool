# Beginner's Guide to the Archival Metadata Utility Tool

**General Setup**
1. Ensure your digital files are connected in a read-only mode via software or hardware to protect them from being altered.
2. Open the tool by navigating to the OMCSERV network drive and opening the Archival Procedure folder and double-clicking on the **archival-metadata-utility-tool.py**.

 ![File Explorer Window](images/File-Explorer.png)
 
 *Image: Navigate to OMC local network drive to open the utility tool*

---

### Option 1: Extract Metadata from a Folder (No Existing Entity Ref IDs)
Use this option if your files have not been uploaded to a system such as Preservica yet and you are extracting the **Technical Metadata** for the first time from the source device.

1. **Choose the Option:** Select Option 1 in the tool.

![Archive Metadata Utility Tool Window](images/Option-1/Select_Option-1.png)

*Image: Archive Metadata Utility Tool Window*
   
2. **Provide Paths:**
   1. Click **Browse Folder** to select the source device.
   2. Click **Browse Folder** to select the **Export to** location for both metadata files.

![Archive Metadata Utility Tool Window](images/Option-1/Select-Folder-Paths.png)

*Image: Archive Metadata Utility Tool Window Selecting Paths*
   
3. **Start Process:** Click the "Start Process" button. The tool will scan your folder to extract technical information and create a new Excel file in your export folder.

![Archive Metadata Utility Tool Window](images/Option-1/Start-Process_1.png)

*Image: Archive Metadata Utility Tool Start Process*
   
4. **Add Descriptions:** When the tool pauses, click the **Open File** button to open the newly created Excel file. Fill in the missing descriptive information in the "DC" tab.

![Archive Metadata Utility Tool Window](images/Option-1/Start-Process_2.png)

*Image: Archive Metadata Utility Tool Window*

![Archive Metadata Utility Tool Window](images/Option-1/Action-Required_Open-FIle.png)

*Image: Action Required: Edit Metadata Pop-up*

![Metadata Excel](images/Option-1/Open_File.png)

*Image: Metadata Working File Excel*
   
5. **Resume Tool:** Save and close the Excel file, then click OK in the tool to resume.

![Archive Metadata Utility Tool Window](images/Option-1/Action-Required_OK.png)

*Image: Action Required: Edit Metadata Pop-up*
   
6. **Finalize:** The tool will check your entries for typos and missing fields, then save the final completed `DC.csv` and Excel files in your export folder.

![Process Complete Window](images/Option-1/Process-Complete.png)

*Image: Process Complete Window*

![Process Complete Window](images/Option-1/Process-Output-Log.png)

*Image: Process Complete Window*

![Process Complete Window](images/Option-1/File-Explorer-DC.png)

*Image: DC File Export*

![Process Complete Window](images/Option-1/DC-Excel.png)

*Image: DC File*

---

### Option 2: Extract Metadata and Add Existing IDs
Use this option if your files are already in Preservica and you need to link them with their existing IDs.

1. **Choose the Option:** Select Option 2 in the tool.


*Image: Archive Metadata Utility Tool Window*
   
2. **Provide Paths:** Enter the folder path containing your digital files, the file path for your Preservica CSV export, and the folder path where you want to save your new exports.

   1. Click **Browse Folder** to select the source device.
   2. Click **Browse File** to select the csv exported from Preservica containing the **Entity Ref ID**.
   3. Click **Browse Folder** to select the **Export to** location for both metadata files.


*Image: Archive Metadata Utility Tool Window Selecting Paths*

3. **Start Process:** Click the "Start Process" button. The tool will scan your folder, match your files with their Preservica IDs, and create a new Excel file in your export folder.

4. **Add Descriptions:** When the tool pauses, open the newly created Excel file. Fill in the missing descriptive information in the "DC" tab.
 
![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/607536c5455b6396580d1b3fc4bc6dbbc6108246/Images/Option-1/Action-Required_Open-FIle.png)

*Image: Action Required: Edit Metadata Pop-up*

![Metadata Excel](https://github.com/ElviraV120/archival_ingest_process/blob/607536c5455b6396580d1b3fc4bc6dbbc6108246/Images/Option-1/Open_File%201.png)

*Image: Metadata Working File Excel*

*Image: Archive Metadata Utility Tool Window*

5. **Resume Tool:** Save and close the Excel file, then click OK in the tool to resume.



*Image: Action Required: Edit Metadata Pop-up*

6. **Finalize:** The tool will check your entries for typos and missing fields, then save the final completed `DC.csv` and Excel files in your export folder.

---

### Option 3: Use an Existing Technical Metadata File
Use this option if you already have a spreadsheet of technical metadata and need to format it or add Preservica IDs.

1. **Choose the Option:** Select Option 3 in the tool.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/2b6ebf089ba3e05711acb60becd83195fe3365ad/Images/Option-3/Select_Option-3.png)

*Image: Archive Metadata Utility Tool Window*

2. **Provide Paths:** Enter the file path of your existing technical metadata file, the file path for your Preservica CSV export, and the folder path where you want to save your new exports.

   1. Click **Browse Folder** to select the source device.
   2. Click **Browse File** to select the csv exported from Preservica containing the **Entity Ref ID**.
   3. Click **Browse Folder** to select the **Export to** location for both metadata files.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/2b6ebf089ba3e05711acb60becd83195fe3365ad/Images/Option-3/Select-Folder-Paths.png)

*Image: Archive Metadata Utility Tool Window Selecting Paths*

3. **Start Process:** Click the "Start Process" button. The tool will load your existing metadata, match your files with their Preservica IDs, and create a new Excel file in your export folder.
   
4. **Add Descriptions:** When the tool pauses, open the newly created Excel file. Fill in the missing descriptive information in the "DC" tab.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-3/Start-Proces_2-1.png)

*Image: Archive Metadata Utility Tool Window*


5. **Resume Tool:** Save and close the Excel file, then click OK in the tool to resume.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-3/Start-Proces_2-2.png)

*Image: Action Required: Edit Metadata Pop-up*

6. **Finalize:** The tool will check your entries for typos and missing fields, then save the final completed `DC.csv` and Excel files in your export folder.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-3/Process-Complete.png)

*Image: Process Complete Window*


---

### Option 4: Resume a Prior Job or Validate an Existing File
Use this option to continue an interrupted job or run the tool's spell-check and validation on an existing metadata file.

1. **Choose the Option:** Select Option 4 in the tool.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-4/Select_Option-4.png)

*Image: Archive Metadata Utility Tool Window*

2. **Provide Paths:** Enter the file path of your existing metadata Excel file and the folder path where you want to save your new exports.

   1. Click **Browse File** to select the **Existing Metadata** file.
   2. Click **Browse Folder** to select the **Export to** location for both metadata files.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-4/Select-Folder-Paths.png)

*Image: Archive Metadata Utility Tool Window Selecting Paths*

3. **Start Process:** Click the "Start Process" button. The tool will load your existing Excel file while preserving your previous work.
   
4. **Add Descriptions:** When the tool pauses, open the Excel file. Fill in any missing descriptive information in the "DC" tab.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-4/Start-Proces_2-1.png)

*Image: Archive Metadata Utility Tool Window*

5. **Resume Tool:** Save and close the Excel file, then click OK in the tool to resume.

![Archive Metadata Utility Tool Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-4/Start-Proces_2-2.png)

*Image: Action Required: Edit Metadata Pop-up*

6. **Finalize:** The tool will check your entries for typos and missing fields, then save the final completed `DC.csv` and Excel files in your export folder.

![Process Complete Window](https://github.com/ElviraV120/archival_ingest_process/blob/fc52de011e1dd9f4d4f973ed4f4cf204029f8d52/Images/Option-4/Process-Complete.png)

*Image: Process Complete Window*

![Process Complete Window](https://github.com/ElviraV120/archival_ingest_process/blob/2b6ebf089ba3e05711acb60becd83195fe3365ad/Images/Option-1/Process-Output-Log.png)

*Image: Process Complete Window*

![Process Complete Window](https://github.com/ElviraV120/archival_ingest_process/blob/607536c5455b6396580d1b3fc4bc6dbbc6108246/Images/Option-1/File-Explorer-DC.png)

*Image: DC File Export*

![Process Complete Window](https://github.com/ElviraV120/archival_ingest_process/blob/2b6ebf089ba3e05711acb60becd83195fe3365ad/Images/Option-1/DC-Excel.png)

*Image: DC File*

Once the last step is completed for any of the chosen options, you have the DC file ready to upload to your Preservica account to ingest the metadata for the assets.
