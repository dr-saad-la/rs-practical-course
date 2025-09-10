# Python Environment Setup Using Miniconda

## What is Miniconda?
Miniconda is a lightweight Python distribution that includes Python and the conda package manager. 

## Step 1: Install Miniconda

### Windows
1. Go to [miniconda.conda-forge.org](https://miniconda.conda-forge.org/)
2. Download the **Windows 64-bit** installer
3. Run the downloaded `.exe` file
4. Follow the installation wizard (accept defaults)
5. **Important**: Check "Add Miniconda3 to PATH" during installation

### Mac

1. Go to [miniconda.conda-forge.org](https://miniconda.conda-forge.org/)
2. Download the **macOS 64-bit** installer
3. Open Terminal and run:
   ```bash
   bash ~/Downloads/Miniconda3-latest-MacOSX-x86_64.sh
   ```
4. Follow the prompts (type "yes" when asked)
5. Restart Terminal

### Linux
1. Open Terminal
2. Download and install:
   ```bash
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
   bash Miniconda3-latest-Linux-x86_64.sh
   ```
3. Follow the prompts (type "yes" when asked)
4. Restart Terminal

## Step 2: Verify Installation

Open a new terminal/command prompt and type:

```bash
conda --version
```

You should see a version number (e.g., `conda 23.1.0`)

In case the command is not recognized, follow the next steps:

1. Open conda prompt (or terminal)
2. run this command
   ```bash
   conda init
   ```
3. Restart the command prompt
4. Run the next command again
   ```bash
   conda --version
   ```

you should see the version this time. 

## Step 3: Create a Virtual Environment

### Create a new environment

```bash
conda create --name myproject python=3.11
```
- Replace `myproject` with your desired project name
- Python 3.11 is recommended (you can use 3.9+ as well)

### Activate the environment

```bash
conda activate myproject
```

### Verify you're in the environment

Your command prompt should now show `(myproject)` at the beginning.

## Step 4: Install Essential Packages

While your environment is activated, install common packages:

```bash
conda install numpy pandas matplotlib jupyter-lab
```

### 5. Resgister The Environment 

Follow the next steps to register the kernel from the conda prompt:

1. Install the kernel
   ```bash
   conda install ipykernel
   ```
2. Register the kernel
   ```bash
   ipython kernel install --user --name="env-name"
   ```

## Quick Reference Commands

| Command | Purpose |
|---------|---------|
| `conda activate myproject` | Activate environment |
| `conda deactivate` | Exit current environment |
| `conda list` | Show installed packages |
| `conda install package_name` | Install a package |
| `conda env list` | Show all environments |

## Tips for Success

1. **Always activate your environment** before working on a project
2. **Create separate environments** for different projects
3. **Use descriptive names** for your environments (e.g., `data_analysis`, `web_scraping`)
4. **Install packages while environment is activated** to keep them project-specific

## Next Steps

Once your environment is set up:
1. Start Jupyter lab: `jupyter lab`
2. Or use any Python IDE/editor of your choice (VS Code, PyCharm)
3. Begin coding with a clean, isolated Python environment!

---

*Your Python development environment is now ready! Each project can have its own environment with specific package versions, keeping everything organized and conflict-free.*