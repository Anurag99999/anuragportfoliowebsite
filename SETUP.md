# Setup Instructions

## Quick Setup (Choose One Method)

### Method 1: Using uv (Recommended)

1. Install uv (if not already installed):
   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

2. Install dependencies:
   ```bash
   uv sync
   ```

3. Generate the site:
   ```bash
   uv run scripts/generate_site.py
   ```

4. Serve locally:
   ```bash
   uv run scripts/dev_server.py
   ```

### Method 2: Using Python Virtual Environment (Recommended if pip has permission issues)

1. Create a virtual environment:
   ```bash
   python3 -m venv venv
   ```

2. Activate the virtual environment:
   ```bash
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   python3 -m pip install -r requirements.txt
   ```

4. Generate the site:
   ```bash
   python3 scripts/generate_site.py
   ```

5. Serve locally (optional, requires livereload):
   ```bash
   python3 -m pip install livereload
   python3 scripts/dev_server.py
   ```

### Method 3: Install Dependencies with python3 -m pip

**Use this if `pip` command is not found:**

```bash
python3 -m pip install jinja2 markdown python-frontmatter markupsafe
python3 scripts/generate_site.py
```

**Or install to user directory (if you get permission errors):**

```bash
python3 -m pip install --user jinja2 markdown python-frontmatter markupsafe
python3 scripts/generate_site.py
```

## Troubleshooting

- If you get "ModuleNotFoundError", make sure you've installed all dependencies
- Make sure you're using Python 3.12 or higher
- If using a virtual environment, make sure it's activated before running scripts

