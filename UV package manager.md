
# Why Use UV?
## Speed Benefits:
- 10-100x faster than pip for package installation
- Parallel downloads and installations
- Better dependency resolution

## Convenience:
- Automatic Python version management
- Built-in virtual environment creation
- Compatible with pip workflows

# Steps to install UV package manager (for Windows 11)

## Install uv package manager
### Option 1: using pip & powershell
```bash
pip install uv
```

### Option 2: using standalone installer
- Open PowerShell as Administrator
- Run the installation command:
```bash
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Verification Steps
```bash
uv --version
```

## Create a Virtual Environment using uv
### Creates a virtual environment in .venv folder
```bash
uv venv
```

### Or specify a custom name/path
```bash
uv venv my-env
```

### Or specify Python version
```bash
uv venv --python 3.11
```

## Activate the Virtual Environment
### If created with default name (.venv)
```bash
.venv\Scripts\Activate.ps1
```

### If created with custom name
```bash
my-env\Scripts\Activate.ps1
```

## Install Packages with UV
### Install single package
```bash
uv pip install requests
```

### Install multiple packages
```bash
uv pip install fastapi uvicorn pandas
```

### Install from requirements.txt
```bash
uv pip install -r requirements.txt
```

### Install with specific versions
```bash
uv pip install "django>=4.0,<5.0"
```

## Deactivate Environment
```bash
deactivate
```



