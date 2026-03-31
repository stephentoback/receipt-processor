# Receipt Processor Web App

Upload multiple receipt PDFs, generate a cover page for each one, prepend it to the original receipt PDF, and save renamed output files.

## File naming format

`VendorName - 00-00 - YYYY-MM-DD - Short Description.pdf`

`00-00` is dollars-cents from total amount (example: `$12.34` => `12-34`).

## Features

- Multi-file PDF upload
- Dynamic metadata form per file
- Cover page added as first page
- Vendor memory (fund code + project + purchase)
- Fund code suggestion when uncertain (must still be confirmed/edited by you)
- Remembers your name for future sessions

## Run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Then open http://127.0.0.1:5000

## Persistence

- Vendor/user memory: `data/vendor_memory.json`
- Output PDFs: `outputs/<your-folder>/`
