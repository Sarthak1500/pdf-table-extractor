# 📝 Hackathon Report: PDF Table Extractor
**🔗 GitHub Repository**: [https://github.com/Sarthak1500/pdf-table-extractor.git](https://github.com/Sarthak1500/pdf-table-extractor.git)


## 📌 Problem Statement

Build a tool that can extract tabular data from system-generated PDF files without using standard libraries like Tabula or Camelot.

## 🎯 Objective

To parse PDF documents and extract tabular data into structured Excel sheets using lightweight and efficient Python tools.

## 🛠️ Tech Stack Used

- **Python 3**
- **PyMuPDF (fitz)** – For parsing and reading PDF content
- **Pandas** – For structuring and handling tabular data
- **OpenPyXL** – To create and write to Excel files

## 🚀 Solution Approach

1. Open the PDF using PyMuPDF.
2. For each page:
   - Extract text blocks and group lines by their Y-coordinate (to form rows).
   - Sort each row’s contents based on X-coordinates (to maintain column order).
3. Store these extracted rows in a DataFrame.
4. Save each page's table into a separate sheet in one Excel file using OpenPyXL.

## 💡 Key Features

- No reliance on Java-based tools
- Handles system-generated PDFs (non-scanned)
- Saves multi-page tables into organized Excel sheets
- Clean output with minimal dependencies

## 📂 Output Example

**Output File**: `tables_final.xlsx`  
**Sheets**: One per PDF page  
**Each Sheet**: Contains the table extracted from that page

## 🧪 Sample Run

```bash
python extract_tables.py "test3.pdf" --output tables_final.xlsx
