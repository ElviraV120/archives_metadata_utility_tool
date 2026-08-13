# Frequently Asked Questions (FAQs)

## Q1: How do I run the script?
A: Navigate to the OMCSERV directoty and double-click on the archival-metadata-utility-tool.py file. This will open the user interface window.

**Note:** You might see a window pop up asking if you want to open the file with python. Click yes to continue.

## Q2: What are the requirements for running the script?
A: You must have Python, pip, openpyxl and pandas installed on the machine (PC or Mac) that you're using. 

## Q3: What are the steps to install Python?
A: **On a PC** : Open powershell and type `winget install Python.Python.3.14`. You must have admin rights to do this or have IT install it.

**On a Mac** : Navigate to the website https://www.python.org/downloads/mac-osx/ and download the latest version of Python. Follow the installation instructions to complete the installation.

## Q4: What are the steps to install pip?
A: Run the command `python -m ensurepip --upgrade` in PowerShell(PC) or Terminal(Mac).

## Q5: What are the steps to install openpyxl?
A: Run the command `pip install openpyxl` in PowerShell(PC) or Terminal(Mac).

## Q6: What are the steps to install pandas?
A: Run the comman `pip install pandas` in PowerShell(PC) or Terminal(Mac).

## Q7: Powershell shows Python error saying it is not installed.
A: Close Powershell and search `Python` in the bottom search bar. If it shows as installed try opening the archival-metadata-utility-tool.py file again. If the problem persists, restart the computer and try again.

## Q8: I tried to open the tool and it opens a black window but nothing happens.
A: Close the window and try to open the file again.

## Q9: What if I need to use the script on a compter that is not connected to the network drive?
A: The {INSERT FOLDER NAME HERE} must be downloaded in its entirity to the working computer and the script must be run from there. Removing or altering any files from the folder may cause errors when runnign the script.

## Q10: I deleted or modified the original script or metadata template by accident. What should I do?
A: Copy the script or template from the OMCSERV drive and paste it in your working directory. If you have altered the copy in the OMCSERV drive the visit the GitHub page to download a fresh copy at https://github.com/ElviraV120/archives_metadata_utility_tool/tree/main

## Q11: What if I manually created or added all my metadata from scratch and want to use it with the script?
A: Ensure you have all the necessary metadata populated in the DC tab of the metadata template and saved. If you have already run the script, you may need to resume it to ensure the metadata is validated and exported correctly.

**Note** : The metadata will only validate an excel or csv file that is formated exactly as the template provided but still export as the Preservica csv format.

## Q12: What if I want to add a controlled vocabulary word or phrase to the list?
A: Open the Metadata_Template.xlsx file located in the OMCSERV drive and add the word or phrase to the bottom of the list in the controlled vocablary tab.
    ![Excel in Edit Mode](images/Option-1/Edit-Mode.png)

**Note** The if you downloaded a copy of the utility tool folder to your computer, you will need to update the metadata template on the network drive as well.
