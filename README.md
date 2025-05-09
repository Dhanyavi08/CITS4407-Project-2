# CITS4407 Assignment 2 — Board Games or Bored Games

This project contains three Bash scripts for analyzing the Board Game Geek dataset, following the cleaning and analysis instructions provided in the assignment brief.

## Files

- **empty_cells**
  - Scans a semicolon-separated dataset and reports the number of empty cells in each column.
  - Usage: `./empty_cells <file> <separator>`

- **preprocess**
  - Cleans the raw dataset by applying the following transformations:
    - Converts `;` to tab-separated format
    - Converts Windows line endings (`\r\n`) to Unix (`\n`)
    - Converts commas in floating point numbers to dots (e.g., `4,5` → `4.5`)
    - Removes non-ASCII characters
    - Generates new unique `/ID` values for missing IDs
  - Usage: `./preprocess <input_file> > cleaned_dataset.tsv`

- **analysis**
  - Analyzes the cleaned dataset to answer four research questions:
    1. Most popular game mechanic
    2. Most popular game domain
    3. Correlation between publication year and rating
    4. Correlation between complexity and rating
  - Usage: `./analysis cleaned_dataset.tsv`

## Git Versioning

This project includes a `.git` repository to demonstrate proper version control practices, including staged commits and a documented commit history.

##  How to Run the Scripts

1. **Make the scripts executable:**
    ```bash
    chmod +x empty_cells preprocess analysis
    ```

2. **Step 1 – Count Empty Cells**
    ```bash
    ./empty_cells bgg_dataset.txt ";"
    ```

3. **Step 2 – Clean the Dataset**
    ```bash
    ./preprocess bgg_dataset.txt > cleaned_dataset.tsv
    ```

4. **Step 3 – Analyze the Cleaned Data**
    ```bash
    ./analysis cleaned_dataset.tsv
    ```


Created for **CITS4407 – Open Source Tools and Scripting**  
University of Western Australia — Semester 1, 2025  
