# Python Installation Documentation

## Technical Requirements
**Note:** Users must have administrative privileges to install software. IT should be contacted to provide these privileges or install the software.
- Internet connectivity is required for downloading the installer.

## Installation

### 1. Download the python installer
  Open PowerShell in Windows Terminal and install Python with: `winget install Python.Python.3.14` and press enter.

### 2. Verify the installation
  Once the installation completes, open the Command Prompt (or PowerShell) and type: `python --version` and press Enter.

You should see an output similar to:
```
Python 3.10.4
```

### 3. Install pip: 
  In Powershell(PC) or Terminal(Mac) type `python -m ensurepip --upgrade` and press Enter.

### 4. Install pandas: 
  In Powershell(PC) or Terminal(Mac) type: `pip install pandas` and press Enter.

### 5. Install openpyxl: 
  In Powershell(PC) or Terminal(Mac) type: `pip install openpyxl` and press Enter.

## Installation Complete

Installation of the necessary Python package and modules is now complete. You can now use the Python script to process the metadata.