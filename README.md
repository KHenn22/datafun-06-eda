# datafun-06-eda
Northwest Data Analytics Fundamentals Week 6

## Setup (clone, venv, install, verify) (2025-09-21)

Follow these commands on macOS (bash) to reproduce what I did: cloning the repo, creating a Python virtual environment, installing dependencies from `requirements.txt`, and verifying the installation.

```bash
# 1) Clone the repository (choose SSH or HTTPS)
# SSH (requires SSH keys configured):
git clone git@github.com:KHenn22/datafun-06-eda.git
# OR HTTPS:
git clone https://github.com/KHenn22/datafun-06-eda.git

# 2) Change into the project directory
cd datafun-06-eda

# 3) (Optional) Check Python version
python3 --version

# 4) Create a virtual environment (recommended name: .venv)
python3 -m venv .venv

# 5) Activate the virtual environment (bash)
source .venv/bin/activate

# 6) Install pip requirements
pip install -r requirements.txt

# 7) Verify installed packages
pip list
```

Notes:
- The `pip list` command prints installed packages in the active venv; that's how I verified packages were installed.
- If you used a different venv name, adjust the `source` path accordingly.
- To deactivate the venv when finished: `deactivate`.
