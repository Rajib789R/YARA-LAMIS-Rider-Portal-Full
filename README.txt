YARA LAMIS Rider Portal — Full Upgrade V5 (Smart Office)
Open index.html in Chrome/Edge (desktop or Android).

V5 NEW FEATURES:
- Global Search bar (top of every page) — search by Rider ID, Name, Mobile, or Vehicle Plate
- Rider 360° Profile — one screen showing a rider's orders, performance, documents,
  penalty history + proof, and assigned vehicle. Open it via the "360°" button on the
  Riders page or by tapping a search result.
- Vehicle Management page — add/update/delete vehicles, assign to riders, track
  registration & insurance expiry dates
- Smart Action Center (Dashboard) — automatically flags:
    - Expired / soon-to-expire rider documents
    - Expired / soon-to-expire vehicle registration & insurance
    - Pending penalties
- Vehicle count added to Dashboard metrics
- Document Vault — three view modes:
    - List view (original table)
    - Gallery view — card + thumbnail per document, expiry badge shown on the card
    - By Rider (folder) view — one folder per rider; open a folder to see every
      document that rider has, with full details (file name, issue/expiry date,
      note/number, upload date, size, thumbnail) and View/Update/Download/Delete
      actions inline
- Excel Reports & Bulk Update (Reports page):
    - "Download Daily Rider Report (Excel)" — real .xlsx file with each rider's
      today's orders/completed, totals, completion %, penalty totals, document
      status count, and assigned vehicle plate
    - "Download Editable Excel Template" — a 3-sheet workbook (Riders,
      Performance, Penalties) pre-filled with current data, ready to edit in Excel
    - "Import Excel to Update Data" — upload the edited workbook back; the app
      reads the Riders / Performance / Penalties sheets, adds new rows and
      updates matching existing ones (matched by Rider ID / Rider ID+Date /
      Penalty ID), then automatically recalculates the Dashboard and all
      analytics — no page reload needed
    - NOTE: this is a manual re-upload, not a live file sync — the browser
      cannot watch or auto-read a file on your computer. Edit the Excel file,
      save it, then click "Import Excel to Update Data" and select it again
      each time you want the analytics refreshed. Requires an internet
      connection the first time to load the Excel engine (from a CDN).
    - "Import ANY Excel File (Preview + Column Mapping)" — for Excel files that
      don't follow the template's exact column names. Upload any .xlsx/.xl
      Same automatic dashboard refresh applies.
- Daily Rider Entry & Ledger (new "Daily Entry" nav item):
    - Search a rider by Rider ID OR Mobile Number in one box — the system
      matches to the correct Rider ID automatically
    - One quick form to enter that day's Orders, Completed, Cancel, Reject,
      Online Hours, and (optionally) a Penalty amount + reason — save once and
      everything links to that Rider ID automatically. If an entry already
      exists for that rider on that date it is updated, not duplicated.
    - Shows the rider's lifetime totals (orders, penalty, days recorded) right
      above the form for context before you enter today's numbers
    - Daily Ledger table below the form lists every rider's day-by-day Orders /
      Completed / Cancel / Reject / that day's Penalty, filterable by date or
      rider name — updates automatically the moment any entry is saved
      anywhere in the app (quick entry, Performance page, or Excel import)

CARRIED OVER FROM V4:
- Rider management
- Performance dashboard
- Document Vault with expiry alerts
- Real file storage via IndexedDB
- PDF/image View + Download + Update + Delete
- Rider-wise penalty management (amount/date/reason/status/reference)
- Penalty evidence file storage and View/Download
- Penalty dashboard metrics
- JSON backup and CSV exports

DATA STORAGE:
- All records (riders, performance, penalties, documents, vehicles, settings) are
  stored in this browser's localStorage.
- Uploaded files (documents & penalty evidence) are stored in this browser's
  IndexedDB, not in localStorage.
- Use Backup (top-right) regularly and keep the JSON file safe -- clearing browser
  data will remove everything stored locally.

PRODUCTION NOTE:
For multi-device / multi-office use, connect a real backend (see
supabase_schema.sql for a starter schema) with authentication and cloud file
storage instead of relying on browser-local storage.
