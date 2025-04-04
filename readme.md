# 📄 PDF Table Extractor

A lightweight Python tool to extract tabular data from system-generated PDFs and save them into an Excel file — **without using Tabula or Camelot**.

**🔗 GitHub Repository**: [https://github.com/Sarthak1500/pdf-table-extractor.git](https://github.com/Sarthak1500/pdf-table-extractor.git)

**🔗 DEMO VIDEO**: [https://drive.google.com/file/d/1c59sLiBGsWvX1xk2tVV6LC3kFFNBDTXv/view?usp=sharing](https://drive.google.com/file/d/1c59sLiBGsWvX1xk2tVV6LC3kFFNBDTXv/view?usp=sharing)

**🔗 OUTPUT EXCEL FILE**: [https://docs.google.com/spreadsheets/d/1yJiNQN-7cFA7ndGTfdD-34KxadpegVID/edit?usp=drive_link&ouid=114446118970431918874&rtpof=true&sd=true](https://docs.google.com/spreadsheets/d/1yJiNQN-7cFA7ndGTfdD-34KxadpegVID/edit?usp=drive_link&ouid=114446118970431918874&rtpof=true&sd=true)



## 🚀 Features

- Extracts tables from **any system-generated PDF** (not scanned)
- Saves each page's table in **separate Excel sheets**
- **No external Java dependencies** (unlike Tabula)
- Clean and readable output using Pandas

## 🛠️ Tech Stack

- Python 3
- [PyMuPDF (fitz)](https://pymupdf.readthedocs.io/) – For parsing PDFs
- Pandas – Data structure and table handling
- OpenPyXL – Excel file creation

## 🧾 How It Works

1. Scans the PDF and groups text lines by Y-coordinate (rows)
2. Sorts text within each row by X-coordinate
3. Builds tables dynamically for each page
4. Outputs everything to Excel

## 📦 Installation

```bash
pip install pymupdf pandas openpyxl
```

## 📂 Usage

```bash
python extract_tables.py input.pdf --output tables.xlsx
```

**Arguments:**
- `input.pdf` – Path to your PDF file
- `--output` – (Optional) Name of output Excel file (default: `extracted_tables.xlsx`)

### 🔍 How to Give the Correct File Path

Make sure to provide the **full absolute path** or correct **relative path** to your PDF. Here are examples:

**Same folder as script:**
```bash
python extract_tables.py report.pdf
```

**From Downloads folder (Windows):**
```bash
python extract_tables.py "C:/Users/YourUsername/Downloads/report.pdf"
```

**From a different folder:**
```bash
python extract_tables.py "D:/Documents/Projects/test.pdf"
```

⚠️ Always wrap the path in quotes if it contains spaces.

## ✅ Example

```bash
python extract_tables.py "test3.pdf" --output tables_final.xlsx
```

## 📄 Output

- One Excel file with multiple sheets: Each sheet corresponds to one page in the PDF.



