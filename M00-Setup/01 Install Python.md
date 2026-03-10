# 01 — Install Python
### Python Development | MCC BSIT 2526

[Back to Setup Overview](./README.md)

---

Python is the programming language this course runs on. We need version **3.10 or higher**.

---

## Windows

1. Go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the **"Download Python 3.x.x"** button
3. Run the downloaded `.exe` file
4. ⚠️ On the first screen, check **"Add Python to PATH"** before clicking anything else

   ```
   ┌─────────────────────────────────────────┐
   │  Install Python 3.x.x                   │
   │                                         │
   │  o Install Now                          │
   │  o Customize installation               │
   │                                         │
   │  [x] Add Python to PATH   <- CHECK THIS │
   └─────────────────────────────────────────┘
   ```

   > ⚠️ If you skip this, Python will not work in the terminal and you will need to reinstall.

5. Click **"Install Now"** and wait for it to finish
6. Click **Close**

**Verify — open Command Prompt and run:**
```
python --version
```
Expected: `Python 3.12.x`

---

## macOS

1. Go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click **"Download Python 3.x.x"**
3. Open the downloaded `.pkg` file and follow the installer steps

**Verify — open Terminal and run:**
```bash
python3 --version
```
Expected: `Python 3.12.x`

> On macOS, always use `python3` instead of `python` in the terminal.

---

## Linux (Ubuntu / Debian)

Check if Python is already installed:
```bash
python3 --version
```

If the version is 3.10 or higher, skip to the next guide.

If it is older or not found:
```bash
sudo apt update
sudo apt install python3 python3-pip -y
```

**Verify:**
```bash
python3 --version
pip3 --version
```

---

## Common Issues

**"python is not recognized" (Windows)**  
You missed the "Add to PATH" checkbox. Uninstall Python from Control Panel, then reinstall and check the box.

**Wrong version showing (e.g. Python 2.7)**  
Install the latest from python.org and use `python3` on macOS/Linux.

**"command not found: python3" (macOS/Linux)**  
Run `sudo apt install python3` on Linux, or reinstall from python.org on macOS.

---

Next: [Install VS Code](./02-Install-VSCode.md)
