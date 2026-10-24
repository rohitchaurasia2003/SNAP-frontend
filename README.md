# SNAP

SNAP is a Flask-powered landing page for an AI-assisted classroom attendance product. It introduces the product’s features and teacher workflow, and links visitors to the separate SNAP attendance application.

## Features

- Responsive landing page with product overview, feature highlights, and teacher workflow.
- Flask serves the page and its static assets.
- Screenshots and logos are stored locally in `static/img/`.
- Links to the SNAP attendance application hosted on Streamlit.

> The attendance application itself is hosted separately and is not part of this repository.

## Requirements

- Python 3.10 or newer
- pip

Dependencies are listed in [`requirements.txt`](./requirements.txt).

## Run locally

From the project root, create and activate a virtual environment, install dependencies, and start the Flask app:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python app.py
```

On Windows PowerShell, activate the environment with:

```powershell
.\.venv\Scripts\Activate.ps1
```

Open [http://127.0.0.1:5002](http://127.0.0.1:5002) in your browser.

## Project structure

```text
.
├── app.py                  # Flask application and home page route
├── requirements.txt        # Python dependencies
├── static/
│   ├── css/
│   │   └── style.css       # Page styles and responsive layout
│   └── img/
│       ├── demo/           # Product and workflow screenshots
│       ├── app_logo.png
│       └── logo.png
└── templates/
    └── index.html          # Landing page template
```

## Configuration

The development entry point in `app.py` serves the site on port `5002`. The external attendance application URL is currently set in `templates/index.html`.

## License

No license is specified in this repository. Add a license file before redistributing the project if one is intended.
