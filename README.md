# VSCode Settings and Extensions 🛠️

### Import VSCode Settings

1. Copy the contents of [settings.json](https://github.com/wazeerc/vsc/blob/master/settings.json).
2. Open VS Code, press `Ctrl + Shift + P`, then type **"Preferences: Open Settings (JSON)"** and press Enter.
3. Press `Ctrl + A` to select all, and `Ctrl + V` to paste and overwrite the current settings.
  
***

### Install Recommended Extensions

#### Option 1: Manual Installation

1. Add [extensions.json](https://github.com/wazeerc/vsc/blob/master/extensions.json) to the `.vscode` folder at the root of your project.
2. This will recommend extensions when users open a project in VS Code.
3. Open the **Extensions** tab and type **@recommended** in the search bar.
4. Install the desired recommended extensions from the list.

#### Option 2: Automated Installation via PowerShell

1. Add `extensions.json` to the `.vscode` folder at the root of your project.
2. Open a Powershell terminal.
3. Run the following PowerShell command to automatically install all recommended extensions:

   ```pwsh
    (Get-Content .vscode/extensions.json | ConvertFrom-Json).recommendations | ForEach-Object { code --install-extension $_ }

