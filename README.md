# VSCode Settings and Extensions 🛠️

### Import VSCode Settings

1. Copy the contents of `settings.json`.
2. Open VS Code and press `Ctrl + Shift + P`, then type **"Preferences: Open Settings (JSON)"**.
3. Press `Ctrl + A` to select all, and `Ctrl + V` to paste and overwrite the current settings.

### Install Recommended Extensions

#### Option 1: Manual Installation

1. Add `extensions.json` to the `.vscode` folder at the root of your project.
2. This will recommend extensions when users open the project in VS Code.
3. Open the **Extensions** tab and expand **Recommended**.
4. Install the desired recommended extensions from the list.

#### Option 2: Automated Installation via PowerShell

1. Add `extensions.json` to the `.vscode` folder at the root of your project.
2. Run the following PowerShell command to automatically install all recommended extensions:

   ```pwsh
    (Get-Content .vscode/extensions.json | ConvertFrom-Json).recommendations | ForEach-Object { code --install-extension $_ }

