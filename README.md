## How to Run the Nicotine Monitoring System

Follow these steps exactly to run the project on your own computer.

### 1. Prerequisites
Make sure you have these installed:
- **Python 3.x** – download from https://www.python.org/downloads/ (check “Add Python to PATH” on Windows).
- **VS Code** (recommended editor) – download from https://code.visualstudio.com/.

### 2. Open the Project Folder
Open the folder that contains `css`, `html`, `js`, and `server` in VS Code. If your download has an extra outer folder with the same project name, open the inner folder.

In VS Code, choose **File > Open Folder...**, select the project folder, and click **Select Folder**. You can also run this from PowerShell while you are in the outer download folder:

```powershell
code .\Nicotine-Withdrawal-Monitoring-System-main
```

In VS Code, open **Terminal > New Terminal**. The terminal should start in the project root (the folder containing `css`, `html`, `js`, and `server`).

The project files should include a structure similar to this. The `.venv` folder is created during setup; it may not be included in the download.

```
project-folder/
├── css/
├── html/
├── js/
├── server/
│   ├── app.py
│   ├── requirements.txt
│   └── ...
├── .venv/               (created during setup)
└── README.md
```

### 3. Setting Up the Backend (Do this once)

1. Make sure the VS Code terminal is in the project root. If you opened the outer download folder instead, change to the inner project folder:
   ```
   cd .\Nicotine-Withdrawal-Monitoring-System-main
   ```
   Skip this command if the terminal is already in the folder containing `css`, `html`, `js`, and `server`.
2. Create a virtual environment:
   ```
   python -m venv .venv
   ```
3. Activate it:
   - **Windows PowerShell**:
     ```
     Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
     .\.venv\Scripts\Activate.ps1
     ```
     The policy change applies only to the current PowerShell window. If you prefer not to activate the environment, use the direct Python commands in Step 4.
   - **Windows Command Prompt**:
     ```
     .\.venv\Scripts\activate.bat
     ```
   - **macOS / Linux**:
     ```
     source .venv/bin/activate
     ```
   You should see `(.venv)` at the start of your command line when activation succeeds.
4. Move into the backend folder:
   ```
   cd .\server
   ```
5. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
   Without activating the environment, use:
   ```
   ..\.venv\Scripts\python.exe -m pip install -r requirements.txt
   ```

### 4. Running the App (Do this every time)
1. Open a terminal in the project root and activate the environment if needed (see Step 3), then move into the backend folder:
   ```
   cd .\server
   ```
2. Start the backend:
   ```
   python app.py
   ```
   Without activating the environment, use:
   ```
   ..\.venv\Scripts\python.exe app.py
   ```
3. Wait for the message `Running on http://127.0.0.1:5000`.
4. Open your browser (Chrome/Edge) and visit `http://localhost:5000`.

### 5. Troubleshooting
- **“Module not found”**: The virtual environment isn’t active or `pip install -r requirements.txt` wasn’t run. Repeat Step 3.
- **PowerShell says running scripts is disabled**: Run `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` in that terminal, then activate with `.\.venv\Scripts\Activate.ps1`. This change is limited to that PowerShell window.
- **“python is not recognized”**: Python isn’t installed or not added to PATH. Reinstall Python and enable the PATH option.
- **“Cannot find path ...\server”**: The terminal is not at the project root. In VS Code, choose **File > Open Folder...** to open the folder containing `css`, `html`, `js`, and `server`, then open a new terminal.
- **Changes not showing?**: Hard-refresh the browser with `Ctrl + Shift + R` to clear cache.




## Credits & Collaboration
- **My Role:** System concept/idea founder, architecture design, and frontend/backend development
- **Team Attribution:** Originally developed collaboratively with S.M Agon, M.J.A Ciervo, M.L Duhan, A.J Redondo for our 3rd-year Data Structures and Algorithms course.
