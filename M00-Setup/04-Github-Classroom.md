# 04 — GitHub Classroom & Cloning Your Repo
### Python Development | MCC BSIT 2526

[Back to Setup Overview](./Setup.md)

---

GitHub Classroom distributes assignments automatically. Each assignment creates a private repository for you — only you and your instructor can see it.

---

## Part A — Accept an Assignment

1. Your instructor will post an invite link on MS Teams for each module. It looks like:  
   `https://classroom.github.com/a/xxxxxxxxx`
2. Click the link and sign in to GitHub if prompted
3. Find your name in the classroom roster and click it — this links your GitHub account to your student record
4. Click **"Accept this assignment"**
5. Wait a few seconds while GitHub creates your repository
6. Click the link to your new repo — it will be named:  
   `https://github.com/mcc-bsit-2526/M01-exercises-your-username`

Your repository is now ready. Only you and your instructor can see it.

---

## Part B — Clone the Repo in VS Code

Cloning downloads your assignment repository to your computer so you can work on it locally.

### Method A — Inside VS Code

1. Open VS Code
2. Press `Ctrl + Shift + P` (Windows/Linux) or `Cmd + Shift + P` (macOS)
3. Type `Git: Clone` and press Enter
4. Paste your repository URL and press Enter
5. Choose a folder to save it in, for example:
   - Windows: `C:\Users\YourName\Documents\PythonDev\`
   - macOS/Linux: `~/Documents/PythonDev/`
6. Click **"Open Repository"** when VS Code asks

### Method B — Terminal

```bash
# Navigate to where you want to save your work
cd Documents

# Clone the repo — replace the URL with yours
git clone https://github.com/mcc-bsit-2526/M01-exercises-your-username.git

# Open it in VS Code
code M01-exercises-your-username
```

---

## Part C — Your Repo Structure

Once cloned, your folder will contain:

```
M01-exercises-your-username/
├── M01_Exercises.ipynb    <- your assignment, work here
├── README.md              <- read this first
├── requirements.txt       <- do not modify
└── test_m01.py            <- do not modify
```

> ⚠️ Do not rename, delete, or modify `test_m01.py` or `requirements.txt`. These are used by the autograder.

---

## Part D — First-Time GitHub Sign-In

The first time VS Code connects to GitHub, a browser window will open asking you to authorize VS Code. Click **"Authorize Visual Studio Code"** and follow the prompts.

If the terminal asks for a password instead, use your Personal Access Token — not your GitHub account password. See [03-Install-Git.md](./03-Install-Git.md) for how to create one.

---

## Common Issues

**"Repository not found" when cloning**  
Make sure you accepted the assignment first and copied the correct URL — your personal repo URL, not the template.

**Cannot find your name in the classroom roster**  
Contact your instructor to be added manually.

**VS Code asks to sign in but nothing happens**  
Try cloning via the terminal using Method B instead.

---

Next: [Using Notebooks](./05-Using-Notebooks.md)
