# Quickstart Guide: Using Python Virtual Environments (venv)
**Version 1.0 | August 2025 | Prepared by Tiffany Smith**  
*Maintained by IT Security Team*

---

## Introduction
This Quickstart guide was prepared by the IT team to help employees use Python safely and consistently.  

While Python is a powerful tool, installing packages without a virtual environment (shortened to “venv”) can cause conflicts that affect other projects or even company systems.  
By following this guide, you’ll learn how to create a safe “workspace” for each project. This reduces errors, improves collaboration, and ensures company data remains secure.

---

## Purpose
This guide shows employees how to safely run Python scripts by using virtual environments (venv).  

A virtual environment keeps your project’s tools and libraries separate so that one project doesn’t accidentally affect or break another.  

Think of it like a **toolbox**: instead of mixing all tools together in one drawer, each project gets its own toolbox.

---

## When to Use This Guide
Use a virtual environment (venv) whenever you:
- Need to run a Python script for work  
- Install new Python packages for a project  
- Work on multiple projects that might use different versions of the same package  

---

## Setting Up Your Python venv

### Step 1: Create a Virtual Environment
Go to your project folder in the terminal, then run:

bash  
python3 -m venv venv

This creates a folder named venv that holds your project’s “toolbox.”

## Step 2: Turn On the Environment
Before running scripts, activate the environment.

- Mac/Linux  
bash  
source venv/bin/activate

- Windows (PowerShell)  
powershell  
venv\Scripts\Activate.ps1

If successful, you’ll see (venv) appear at the start of your command line.

## Step 3: Install Packages
While the environment is active, install packages like this:

bash  
pip install requests

Everything stays inside the project’s toolbox — not on your computer as a whole.

## Step 4: Turn Off the Environment
When you’re done, type:

bash  
deactivate

This safely closes the toolbox.

---

## Best Practices
- Always use python3 instead of python to avoid version conflicts.
- Create one environment per project to prevent software clashes.
- Never email or upload your venv folder.
- Instead, share your requirements file:

bash  
pip freeze > requirements.txt

Colleagues can then re-create your environment with:

bash  
pip install -r requirements.txt

---

## Troubleshooting (Common Fixes)
❌ Command not found: python3  
→ Python isn’t installed or isn’t on your PATH. Contact IT.  
❌ No module named venv  
→ Ask IT to install the Python venv package.  
❌ Still not working?  
✅ Check if (venv) appears at the start of your command line.  
✅ Reactivate with the correct command:

Mac/Linux: source venv/bin/activate

Windows (CMD): venv\Scripts\activate.bat

Windows (PowerShell): venv\Scripts\Activate.ps1

---

## Glossary (Plain Language)
- Python: A programming language designed to be easy to read and use.
- Virtual environment (venv): A private copy of Python + tools for one project.
- Package: A set of Python code that adds features (like Excel add-ins).
- bash: A common terminal (command-line tool) on Mac and Linux.
- PowerShell: The Windows version of a terminal (command-line tool).
- requirements.txt: A text file listing all the packages your project uses.

---

###Revision History
- v1.0 (August 2025) – Initial version
- v1.1 (September 2025) – Revised for clarity, error screenshots added
