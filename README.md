# Monthly Reconciliation (GitHub Pages)

A browser-based tool to compare a Client spreadsheet with a 5C/Internal spreadsheet, identify unmatched study/case IDs, and export the mismatches to Excel.

## Files
- `index.html` — complete application (HTML, CSS, JavaScript).

## Publish on GitHub Pages
1. Create a new GitHub repository (Public is simplest for Pages).
2. Upload `index.html` to the repository root. Keep the filename exactly `index.html`.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then click **Save**.
6. Wait for the Pages deployment to finish. Your site will be available at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

## How to use
1. Open the published page in Chrome or Edge.
2. Upload the Client and 5C/Internal Excel or CSV files.
3. Select the common unique identifier (for example, Study ID).
4. Click **Compare files**.
5. Review both mismatch tabs and choose **Export Excel**. The workbook contains two mismatch sheets and a summary sheet. Original spreadsheet row numbers are included.

## Important
- Files are processed in the browser; the application does not send spreadsheet contents to a backend.
- SheetJS is loaded from jsDelivr CDN. The first load requires access to `cdn.jsdelivr.net`; a restrictive hospital firewall may block it.
- GitHub Pages hosts the static app, but cannot bypass network restrictions imposed by a hospital.
- Test with copies of your files before relying on results. Duplicate identifiers are treated as one key for matching; rows with blank identifiers are skipped.
