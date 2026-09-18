# Image Mass Downloader

Download image search results for many character names from a CSV or Excel spreadsheet.

## Setup

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
```

## Spreadsheet format

Use a CSV or XLSX file with a header named `name` and one character per row. `characters.csv` is included as an example.

## Run

```powershell
py image_downloader.py characters.csv --count 5
```

For an Excel file or a different column name:

```powershell
py image_downloader.py characters.xlsx --column Character --count 10 --output my_images
```

The program creates one folder per character and writes `download_report.csv` with the result of each search. Use `--unsafe` only when you intentionally want to disable safe search.

## Notes

Image providers and websites can have rate limits and usage restrictions. Review image licenses and terms before using downloaded images in a public or commercial project.
