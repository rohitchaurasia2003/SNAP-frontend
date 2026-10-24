# SNAP Frontend

SNAP Frontend is the marketing and landing-page application for an AI-powered classroom attendance system. It presents the product value, workflow, and feature set to teachers and administrators while linking them to the separate SNAP attendance application.

## Overview

This repository contains the public-facing Flask site for SNAP. The interface highlights the product’s AI-driven attendance experience, including face recognition, voice-based verification, QR-powered enrollment, and classroom workflow steps.

> The main attendance application itself is hosted separately and is not included in this repository.

## Features

- Responsive landing page for the SNAP product
- Teacher-focused product messaging and UI sections
- Feature cards for AI face analysis, voice verification, and QR-driven class setup
- Guided classroom workflow highlighting the attendance journey
- Static assets and screenshots stored locally under `static/img/`
- CTA links to the live SNAP attendance app

## Tech Stack

- Python 3.10+
- Flask
- Jinja templates
- HTML/CSS/JavaScript
- Vercel deployment configuration

## Project Structure

```text
.
├── app.py                 # Flask app entry point
├── vercel.json            # Vercel deployment configuration
├── requirements.txt       # Python dependencies
├── static/
│   ├── css/
│   │   └── style.css      # Main styling and responsive layout
│   └── img/
│       ├── demo/          # Product screenshots and workflow visuals
│       ├── app_logo.png
│       └── logo.png
├── templates/
│   └── index.html         # Landing page template
└── README.md              # Project documentation
```

## Requirements

- Python 3.10 or newer
- pip

Install dependencies from:

```bash
pip install -r requirements.txt
```

## Run Locally

From the project root, run:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python app.py
```

On Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
python app.py
```

Then open:

```text
http://127.0.0.1:5002
```

## Deployment

This project is configured for deployment on Vercel using `vercel.json` and the Flask app entry point in `app.py`.

The relevant deployment setup is:

```json
{
  "version": 2,
  "builds": [{ "src": "app.py", "use": "@vercel/python" }],
  "routes": [{ "src": "/(.*)", "dest": "app.py" }]
}
```

## Configuration Notes

- The Flask app runs on port `5002` in local development.
- The live attendance app URL is referenced in `templates/index.html`.
- If you want to update the external product URL, edit the CTA links in the landing page template.

## License

No license is currently specified for this project. If you plan to distribute or reuse it publicly, add an appropriate license file.
