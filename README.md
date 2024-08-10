# RecSam Workflow

## Overview

The `RecSam` workflow is an automation script designed for UiPath that interacts with both Google Chrome and Notepad applications. This workflow performs a series of actions, including opening Google Chrome, typing a search query, extracting a value from a webpage, and then working with Notepad to save the extracted value to a file.

## Features

- **Open Google Chrome**: Starts a new instance of Google Chrome and performs a search.
- **Extract Data**: Retrieves a specific value (SPAN text) from the search results.
- **Open Notepad**: Launches Notepad and inputs the extracted value.
- **Save File**: Saves the Notepad file with a predefined name and closes the application.

## Workflow Details

### 1. Open Google Chrome

- **Action**: `StartProcess`
- **Details**: Launches `chrome.exe` to open a new tab.

### 2. Perform Search in Chrome

- **Action**: `TypeInto`
- **Details**: Types the query "sports" and presses Enter.

### 3. Extract Data from Webpage

- **Action**: `GetValue`
- **Details**: Retrieves the text from a SPAN element on the search results page.

### 4. Open Notepad

- **Action**: `OpenApplication`
- **Details**: Launches `notepad.exe` to create a new document.

### 5. Input Data into Notepad

- **Action**: `TypeInto`
- **Details**: Types the extracted text into the Notepad document.

### 6. Save File

- **Action**: `TypeInto`
- **Details**: Types the file name `file1.txt` into the "Save as" dialog and saves the file.

### 7. Close Applications

- **Actions**: `Click`
- **Details**: Closes the Notepad and Google Chrome applications.

## Usage

1. **Set Up**: Ensure UiPath Studio is installed and properly configured.
2. **Import Workflow**: Import the `RecSam.xaml` file into UiPath Studio.
3. **Configure Paths**: Update paths if necessary (e.g., Notepad and Chrome executable paths).
4. **Run**: Execute the workflow to automate the described tasks.

## Requirements

- UiPath Studio
- Google Chrome installed
- Notepad application

## Known Issues

- Ensure that the selectors used in the `TypeInto`, `GetValue`, and `Click` activities are accurate and match the current UI elements.

## License

This workflow is provided under the [MIT License](LICENSE).
