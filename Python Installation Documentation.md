# Python Installation Documentation

## Technical Requirements
- Users must have administrative privileges to install software. IT should be contacted to provide these privileges or install the software.
- Internet connectivity is required for downloading the installer.

## Python Installation

1. **Download the installer**: 
    Open PowerShell in Windows Terminal and install Python:
`winget install Python.Python.3.14`

2. **Verify the installation**:
   Once the installation completes, open the Command Prompt (or PowerShell) and type:
`python --version`

You should see output similar to:
```
Python 3.10.4
```

1. **Install pip**: 

  In Powershell(PC) or Terminal(Mac) type

   `python -m ensurepip --upgrade`

   and press Enter. 

2. **Install pandas**: 
  
    In Powershell(PC) or Terminal(Mac) type:

   `pip install pandas`

  and press Enter.

3. **Install openpyxl**: 

    In Powershell(PC) or Terminal(Mac) type:

   `pip install openpyxl`

   and press Enter.

## Installation Complete

Installation of the necessary Python package and modules is now complete. You can now use the Python script to process the metadata.