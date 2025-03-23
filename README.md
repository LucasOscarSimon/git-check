# 🔍 git-files-status

A simple, extensible command-line tool to analyze which files in a Git repository are **ignored**, **tracked**, or **untracked**.  
It outputs a clean **Markdown report** by default and optionally a **CSV file** for deeper analysis.  
Also supports printing the results directly in the terminal.

---

## 🚀 Features

- ✅ Detects if you're inside a Git repository  
- 📝 Generates a versioned Markdown report with detailed file classification  
- 📁 Optionally generates a CSV version (`--csv`)  
- 🖥️ Optional `--show` flag to print results in the terminal  
- 🔢 Tracks execution count with auto-incremented report versioning (v1, v2, ...)  
- 📊 Includes a visual summary: totals, percentages, and breakdowns  

---

## 📦 Installation

### Manual (recommended)

1. Clone or download the script:

```bash
git clone https://github.com/your-user/git-files-status.git
cd git-files-status
chmod +x git-files-status
```

2. Move the script to a folder in your PATH (e.g. `~/.local/bin/`):

```bash
mv git-files-status ~/.local/bin/
```

3. Make sure `~/.local/bin/` is in your `PATH`. Add this to your `~/.bashrc`, `~/.zshrc`, or equivalent:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

4. Reload your shell:

```bash
source ~/.zshrc    # or ~/.bashrc, depending on your shell
```

Now you can run it from any Git repository:

```bash
git-files-status
```

---

## 🧪 Usage

```bash
git-files-status [--show] [--csv]
```

### Flags

| Flag     | Description                                      |
|----------|--------------------------------------------------|
| `--show` | Print the output in the terminal                 |
| `--csv`  | Also export a CSV report (in addition to Markdown) |
| `--help` | Show usage information                           |

### Example

```bash
git-files-status --csv --show
```

This will:

- ✅ Show the results in the terminal  
- 📝 Generate a Markdown file: `reports/git_files_report_v1.md`  
- 📁 Generate a CSV file: `reports/git_files_report_v1.csv`  

Each execution generates a new version (`v2`, `v3`, etc.), so nothing is overwritten.

---

## 🛠️ Requirements

- Git must be installed and available in your system  
- Python 3.x (if your script is written in Python)  
- Works on Linux, macOS, and WSL
