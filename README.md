# Notebook Starter

A starter repository for Jupyter notebooks with pre-configured data science packages and project structure.

## Features

- Pre-configured Jupyter environment with popular data science packages
- Organized project structure with `notebooks/` and `data/` directories
- Virtual environment management for reproducible development
- Ready-to-use kernel configuration

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Git (for cloning the repository)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd notebook-starter
```

### 2. Create a Virtual Environment

Create a new virtual environment to isolate your project dependencies:

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment

**On Linux/macOS:**
```bash
source .venv/bin/activate
```

**On Windows:**
```bash
.venv\Scripts\activate
```

You should see `(.venv)` at the beginning of your command prompt when the virtual environment is active.

### 4. Install Required Packages

Install all the required packages from `requirements.txt`:

```bash
pip install -r requirements.txt
```

This will install the following packages:
- `jupyter` - Jupyter core functionality
- `notebook` - Jupyter notebook interface
- `ipykernel` - IPython kernel for Jupyter
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computing
- `matplotlib` - Plotting library
- `seaborn` - Statistical data visualization
- `scikit-learn` - Machine learning library

### 5. Install a Jupyter Kernel for the Virtual Environment

Install a Jupyter kernel that uses the Python interpreter from your virtual environment:

```bash
python -m ipykernel install --user --name=notebook-starter --display-name="Python (notebook-starter)"
```

This creates a kernel named "Python (notebook-starter)" that you can select when creating or running notebooks. The kernel will use the Python interpreter and packages from your virtual environment.

### 6. Launch Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

This will open Jupyter in your default web browser. You can also use:

```bash
jupyter lab
```

For the more modern JupyterLab interface.

## Usage

### Creating a New Notebook

1. Navigate to the `notebooks/` directory in Jupyter
2. Click "New" → "Python (notebook-starter)" to create a new notebook
3. Your notebook will use the virtual environment with all installed packages

### Recommended Project Structure

```
notebook-starter/
├── notebooks/          # Your Jupyter notebooks
├── data/              # Data files and datasets
├── requirements.txt    # Python package dependencies
├── .venv/             # Virtual environment (created during setup)
└── README.md          # This file
```

### Working with Data

- Place your data files in the `data/` directory
- Use relative paths from your notebooks: `../data/your_file.csv`
- The `data/` directory is included in `.gitignore` by default to avoid committing large files

### Package Management

To add new packages to your environment:

1. Activate your virtual environment
2. Install the package: `pip install package_name`
3. Update requirements.txt: `pip freeze > requirements.txt`

## Troubleshooting

### Kernel Not Found
If you don't see the "Python (notebook-starter)" kernel:
1. Ensure your virtual environment is activated
2. Re-run the kernel registration command
3. Restart Jupyter

### Package Import Errors
If you get import errors in notebooks:
1. Check that you're using the correct kernel
2. Verify the virtual environment is activated
3. Reinstall packages: `pip install -r requirements.txt`

### Virtual Environment Issues
If you need to recreate the virtual environment:
```bash
rm -rf .venv
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
python -m ipykernel install --user --name=notebook-starter --display-name="Python (notebook-starter)"
```

## Deactivating the Virtual Environment

When you're done working, deactivate the virtual environment:

```bash
deactivate
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Update `requirements.txt` if you add new dependencies
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.