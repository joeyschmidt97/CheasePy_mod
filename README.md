# Project Setup

## Environment Setup

### 1. Create Conda Environment

Create the conda environment from the `environment.yml` file:

```bash
conda env create -f env/environment.yml
```

### 2. Activate Environment

```bash
conda activate cheasepy
```

## Python Path Configuration

This project uses the import format `REPO.src.file` for clarity. You need to add the parent directory to your `PYTHONPATH` (the dir **ABOVE** this repo).

### Temporary Setup (Current Session)

**Linux/Mac:**
```bash
export PYTHONPATH="${PYTHONPATH}:$(dirname $(pwd))"
```

**Windows (Command Prompt):**
```cmd
set PYTHONPATH=%PYTHONPATH%;%cd%\..
```

**Windows (PowerShell):**
```powershell
$env:PYTHONPATH += ";$(Split-Path -Parent $PWD)"
```

### Permanent Setup

**Linux/Mac:**

Add to your `~/.bashrc` or `~/.zshrc`:
```bash
export PYTHONPATH="${PYTHONPATH}:/path/to/parent/directory"
```

Then reload:
```bash
source ~/.bashrc  # or ~/.zshrc
```

**Windows:**

1. Search for "Environment Variables" in Windows settings
2. Add or edit the `PYTHONPATH` variable
3. Add the path to the parent directory containing this repo

