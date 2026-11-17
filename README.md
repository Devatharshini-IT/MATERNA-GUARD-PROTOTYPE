
  # Materna Guard

  Materna Guard is a React + TypeScript frontend with a Flask API for maternal monitoring, report extraction, risk comparison, and alerts.

  ## Running the code

  Install frontend dependencies:

  ```powershell
  npm install
  ```

  Install Flask and report-extraction dependencies:

  ```powershell
  python -m pip install -r backend/requirements.txt
  ```

  Start the frontend:

  ```powershell
  npm run dev
  ```

  Start Flask in a second terminal:

  ```powershell
  python backend/app.py
  ```

  The application opens at `/dashboard`. Use `/monitoring` for live readings, `/previous-report` to upload a PDF or image for Flask extraction, and `/risk-trend` for automatic previous/current comparison.

  Image OCR requires the Tesseract executable installed and available on `PATH`. PDF text extraction works with `pypdf`; scanned PDFs may need to be supplied as an image or processed with an OCR-enabled PDF tool.

  To test the flow, start both servers, sign in, change readings under Current Monitoring, upload a real report under Previous Report, and open Risk Trend Analysis. The trend page updates from React state without a Compare button or page refresh. Telegram/SMS alert behavior remains configured through `backend/.env`.
  